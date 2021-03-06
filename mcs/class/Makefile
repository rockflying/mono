thisdir = class

pcl_facade_dirs := Facades

# The minimal set of csc dependencies
basic_SUBDIRS := \
	corlib \
	Mono.Security \
	System \
	System.XML \
	System.Core \
	System.ComponentModel.Composition.4.5 \
	System.Numerics \
	System.Xml.Linq \
	System.Runtime.InteropServices.RuntimeInformation \
	Mono.Cecil \
	../tools/cil-stringreplacer

# resgen is corlib specific so we need to wait until corlib is build
# and build it just a step before first dll needs it
resgen_dir = ../tools/resgen

build_SUBDIRS :=  \
	corlib \
	Mono.Security \
	System \
	System.XML \
	Mono.Posix \
	System.Core \
	System.ComponentModel.Composition.4.5 \
	System.Numerics \
	System.Xml.Linq \
	System.Runtime.InteropServices.RuntimeInformation \
	Mono.Cecil \
	../tools/cil-stringreplacer

-include ../build/config.make

ifdef MCS_MODE
basic_PARALLEL_SUBDIRS := ../mcs
build_PARALLEL_SUBDIRS := ../mcs
else
basic_PARALLEL_SUBDIRS := $(pcl_facade_dirs)
build_PARALLEL_SUBDIRS := $(pcl_facade_dirs)
endif

mobile_common_dirs := \
	corlib	\
	Mono.Security \
	System	\
	System.Core	\
	System.Security	\
	System.XML	\
	I18N		\
	System.ServiceModel.Internals	\
	System.Runtime.Serialization	\
	System.Xml.Linq	\
	System.IdentityModel		\
	System.ServiceModel	\
	System.ServiceModel.Web	\
	System.Json	\
	System.Web.Services	\
	Mono.Data.Tds	\
	System.Transactions	\
	System.Numerics	\
	System.Numerics.Vectors		\
	System.Data	\
	Mono.Data.Sqlite	\
	System.Data.Services.Client \
	System.IO.Compression \
	System.IO.Compression.FileSystem \
	System.ComponentModel.DataAnnotations \
	System.ComponentModel.Composition.4.5 \
	System.Net \
	System.Net.Http	\
	System.Windows \
	System.Xml.Serialization \
	Mono.CSharp	\
	Microsoft.CSharp \
	System.Runtime.InteropServices.RuntimeInformation	\
	System.Reflection.DispatchProxy	\
	System.Xml.XPath.XmlDocument \
	System.Reflection.Context	\
	System.Net.Http.WinHttpHandler

aot_only_dirs := \
	$(mobile_common_dirs)	\
	Mono.Dynamic.Interpreter	\
	Mono.CompilerServices.SymbolWriter	\
	Mono.Simd			\
	$(pcl_facade_dirs)

aot_hybrid_dirs := \
	$(mobile_common_dirs)	\
	Mono.CompilerServices.SymbolWriter	\
	Mono.Simd			\
	$(pcl_facade_dirs)

xammac_dirs := \
	$(mobile_common_dirs)	\
	Mono.CompilerServices.SymbolWriter	\
	$(pcl_facade_dirs)

monodroid_dirs := \
	$(mobile_common_dirs)	\
	Mono.CompilerServices.SymbolWriter	\
	Mono.Btls.Interface	\
	$(pcl_facade_dirs)

monotouch_dirs := \
	$(aot_only_dirs)

monotouch_watch_dirs := $(filter-out Mono.Security Mono.Data.Tds,$(monotouch_dirs))
monotouch_tv_dirs   := $(monotouch_dirs)

monotouch_runtime_dirs := \
	corlib \
	Mono.Security \
	System \
	System.Core \
	System.XML \
	Mono.CSharp

monotouch_watch_runtime_dirs := $(filter-out Mono.Security Mono.Data.Tds,$(monotouch_runtime_dirs))
monotouch_tv_runtime_dirs := $(monotouch_runtime_dirs)

xammac_4_5_dirs := \
	corlib	\
	Mono.Security \
	System	\
	Mono.Posix			\
	System.Core	\
	System.Security			\
	System.XML	\
	I18N		\
	System.ServiceModel.Internals	\
	SMDiagnostics	\
	System.Numerics	\
	System.Numerics.Vectors		\
	Mono.Data.Tds	\
	System.Transactions	\
	System.EnterpriseServices	\
	System.Data	\
	System.Runtime.Serialization	\
	System.Xml.Linq	\
	Mono.Data.Sqlite	\
	System.Runtime.Serialization.Formatters.Soap \
	System.ComponentModel.DataAnnotations \
	System.IdentityModel		\
	System.IdentityModel.Selectors	\
	Mono.Messaging			\
	System.Configuration.Install 	\
	System.Messaging	        \
	System.Web.Services \
	System.ServiceModel	\
	System.ServiceModel.Web	\
	System.Json	\
	System.Data.Services.Client \
	System.IO.Compression \
	System.IO.Compression.FileSystem \
	System.ComponentModel.Composition.4.5 \
	System.Net \
	System.Windows \
	System.Xml.Serialization \
	Mono.CSharp	\
	Microsoft.CSharp \
	Mono.CompilerServices.SymbolWriter	\
	System.Data.Linq		\
	System.Net.Http \
	System.Net.Http.WebRequest \
	System.Runtime.InteropServices.RuntimeInformation \
	System.Reflection.Context	\
	System.Net.Http.WinHttpHandler	\
	$(pcl_facade_dirs)

net_4_x_dirs := \
	corlib				\
	Mono.Security \
	System				\
	System.XML			\
	Mono.CompilerServices.SymbolWriter \
	Mono.Posix			\
	System.Core			\
	System.Security			\
	System.Configuration	\
	$(resgen_dir)			\
	System.IO.Compression 		\
	System.IO.Compression.FileSystem \
	System.Drawing			\
	System.Transactions		\
	System.EnterpriseServices	\
	Mono.Data.Tds			\
	System.Numerics		\
	System.Numerics.Vectors		\
	System.Data			\
	System.ComponentModel.DataAnnotations	\
	Accessibility			\
	Mono.WebBrowser			\
	System.Runtime.Serialization.Formatters.Soap \
	System.Windows.Forms		\
	Mono.Data.Sqlite		\
	System.Web.ApplicationServices	\
	Novell.Directory.Ldap		\
	System.DirectoryServices	\
	System.Web			\
	System.Web.Services		\
	System.Design			\
	System.Runtime.Remoting		\
	System.Configuration.Install 	\
	System.Management		\
	System.Data.OracleClient	\
	Cscompmgd			\
	Commons.Xml.Relaxng		\
	Mono.Messaging			\
	System.Messaging	        \
	System.ServiceProcess           \
	System.Drawing.Design		\
	ICSharpCode.SharpZipLib		\
	IBM.Data.DB2			\
	CustomMarshalers		\
	SystemWebTestShim			\
	System.ServiceModel.Internals	\
	SMDiagnostics	\
	System.Runtime.Serialization	\
	System.Xml.Linq			\
	System.Data.Linq		\
	System.Web.Abstractions		\
	System.Web.Routing		\
	System.Runtime.DurableInstancing \
	System.IdentityModel		\
	System.IdentityModel.Selectors	\
	System.ServiceModel		\
	System.Web.Extensions		\
	System.Web.Extensions.Design	\
	System.Web.DynamicData		\
	Mono.CSharp			\
	System.Net			\
	System.Json		\
	Microsoft.CSharp	\
	System.Xaml \
	WindowsBase \
	System.ServiceModel.Activation \
	System.ServiceModel.Routing \
	System.ServiceModel.Discovery \
	System.Runtime.Caching \
	Microsoft.Web.Infrastructure \
	System.ServiceModel.Web \
	System.Net.Http	\
	System.Net.Http.WebRequest \
	System.Web.Razor \
	System.Web.WebPages.Deployment \
	System.Web.WebPages \
	System.Web.WebPages.Razor \
	System.Web.Mvc3 \
	System.Net.Http.Formatting \
	System.Web.Http \
	System.Web.Http.SelfHost \
	System.Web.Http.WebHost \
	System.Runtime.InteropServices.RuntimeInformation

# These are the subdirs which depends on libs in net_4_x_dirs
# or have proper dependencies between each other
net_4_x_parallel_dirs := \
	PEAPI				\
	I18N				\
	Mono.Btls.Interface		\
	Mono.Http			\
	Mono.Cairo                      \
	Mono.Cecil			\
	Mono.Cecil.Mdb			\
	Mono.Debugger.Soft		\
	Mono.C5				\
	Mono.Management			\
	Mono.Options 			\
	Mono.Simd			\
	Mono.Tasklets       		\
	Mono.CodeContracts \
	Mono.Parallel \
	Mono.Security.Win32		\
	Mono.Messaging.RabbitMQ		\
	System.Dynamic			\
	System.Windows.Forms.DataVisualization	\
	System.Reactive.Interfaces \
	System.Reactive.Core \
	System.Reactive.Linq \
	System.Reactive.PlatformServices \
	System.Reactive.Providers \
	System.Reactive.Runtime.Remoting \
	System.Reactive.Windows.Forms \
	System.Reactive.Windows.Threading \
	System.Reactive.Observable.Aliases \
	System.Reactive.Experimental \
	System.Reactive.Debugger \
	System.Data.Services.Client	\
	System.Data.Services \
	System.Data.Entity \
	System.Data.DataSetExtensions	\
	System.Json.Microsoft \
	System.Threading.Tasks.Dataflow \
	System.ComponentModel.Composition.4.5 \
	System.Windows \
	System.Xml.Serialization \
	System.DirectoryServices.Protocols	\
	RabbitMQ.Client			\
	Microsoft.VisualC		\
	WebMatrix.Data \
	monodoc	\
	System.Deployment \
	System.Web.Mobile \
	System.Web.RegularExpressions \
	System.Workflow.Activities \
	System.Workflow.ComponentModel \
	System.Workflow.Runtime \
	System.Reflection.Context \
	legacy/Mono.Cecil \
	$(pcl_facade_dirs)

xbuild_2_0_dirs := \
	Microsoft.Build.Framework	\
	Microsoft.Build.Utilities	\
	Microsoft.Build.Engine		\
	Mono.XBuild.Tasks		\
	Microsoft.Build.Tasks

xbuild_4_0_dirs := \
	$(xbuild_2_0_dirs)	\
	Microsoft.Build

monodroid_SUBDIRS := $(monodroid_dirs)
monotouch_SUBDIRS := $(monotouch_dirs)
monotouch_watch_SUBDIRS := $(monotouch_watch_dirs)
monotouch_tv_SUBDIRS    := $(monotouch_tv_dirs)
monotouch_runtime_SUBDIRS := $(monotouch_runtime_dirs)
monotouch_watch_runtime_SUBDIRS := $(monotouch_watch_runtime_dirs)
monotouch_tv_runtime_SUBDIRS := $(monotouch_tv_runtime_dirs)
aot_only_SUBDIRS := $(aot_only_dirs)
aot_hybrid_SUBDIRS := $(aot_hybrid_dirs)
xammac_SUBDIRS := $(xammac_dirs)
xammac_net_4_5_SUBDIRS := $(xammac_4_5_dirs)
binary_reference_assemblies_SUBDIRS := reference-assemblies
net_4_x_SUBDIRS := $(net_4_x_dirs) $(xbuild_4_0_dirs)
net_4_x_PARALLEL_SUBDIRS := $(net_4_x_parallel_dirs)
xbuild_12_SUBDIRS := $(xbuild_4_0_dirs)
xbuild_14_SUBDIRS := $(xbuild_4_0_dirs) Microsoft.NuGet.Build.Tasks

include ../build/rules.make

SUBDIRS = $(aot_only_dirs) $(aot_hybrid_dirs) $(monotouch_dirs) $(monodroid_dirs) $(xammac_dirs) $(net_4_x_dirs) $(net_4_x_parallel_dirs) $(xammac_net_4_5_SUBDIRS)

DIST_ONLY_SUBDIRS = dlr aot-compiler reference-assemblies $(xbuild_4_0_dirs) Microsoft.NuGet.Build.Tasks

# No new makefiles for: System.Messaging, System.Web.Mobile,
# System.ServiceProcess

DISTFILES = \
	ecma.pub		\
	winfx.pub		\
	winfx3.pub		\
	mono.pub		\
	msfinal.pub		\
	silverlight.pub		\
	reactive.pub		\
	mono.snk		\
	LICENSE 		\
	README			\
	doc/API-notes		\
	doc/NUnitGuidelines	\
	doc/TemplateTest.cs	\
	notes/BitVecto32.txt	\
	MicrosoftAjaxLibrary/License.htm	\
	test-helpers/NetworkHelpers.cs	\
	test-helpers/SocketResponder.cs	\
	lib/$(monolite_dir)/mcs.exe   \
	$(monolite_files)

.PHONY: all-local $(STD_TARGETS:=-local)
all-local $(STD_TARGETS:=-local):
	@:

all-local-aot:

monolite_dir := monolite

# Files needed to bootstrap C# compiler
build_files = mscorlib.dll System.dll System.Xml.dll Mono.Security.dll System.Core.dll System.Security.dll System.Configuration.dll \
	System.Numerics.dll System.Xml.Linq.dll System.Runtime.InteropServices.RuntimeInformation.dll \
	Facades/System.Collections.Concurrent.dll Facades/System.Linq.dll Facades/System.Runtime.dll Facades/System.Collections.dll	\
	Facades/System.Reflection.Extensions.dll Facades/System.Text.Encoding.Extensions.dll Facades/System.Diagnostics.Debug.dll \
	Facades/System.Reflection.Primitives.dll Facades/System.Text.Encoding.dll Facades/System.Diagnostics.Tools.dll Facades/System.Reflection.dll \
	Facades/System.Threading.Tasks.Parallel.dll Facades/System.Dynamic.Runtime.dll Facades/System.Resources.ResourceManager.dll \
	Facades/System.Threading.Tasks.dll Facades/System.Globalization.dll Facades/System.Runtime.Extensions.dll Facades/System.Threading.dll \
	Facades/System.IO.dll Facades/System.Runtime.InteropServices.dll Facades/System.Xml.ReaderWriter.dll Facades/System.Linq.Expressions.dll \
	Facades/System.Runtime.Numerics.dll Facades/System.Xml.XDocument.dll Facades/System.IO.FileSystem.Primitives.dll Facades/System.IO.FileSystem.dll \
	Facades/System.Diagnostics.FileVersionInfo.dll Facades/System.Security.Cryptography.Primitives.dll Facades/System.Security.Cryptography.Algorithms.dll \
	Facades/System.ValueTuple.dll

monolite_files = $(build_files:%=lib/$(monolite_dir)/%)

lib/$(monolite_dir):
lib/$(monolite_dir)/Facades:
	$(MKINSTALLDIRS) $@

$(monolite_files): | lib/$(monolite_dir)
$(monolite_files): | lib/$(monolite_dir)/Facades
$(monolite_files): lib/$(monolite_dir)/%: lib/build/%
	cp -p $< $@

lib/$(monolite_dir)/mcs.exe:
	$(MAKE) -C ../mcs PROFILE=basic
	cp -p lib/basic/mcs.exe lib/$(monolite_dir)

$(build_files:%=lib/build/%):
	cd $(topdir) && $(MAKE) profile-do--build--all NO_DIR_CHECK=1 SKIP_AOT=1

dist-monolite: $(monolite_files) lib/$(monolite_dir)/mcs.exe

dist-default: dist-monolite

dist-local: dist-default

csproj-local:

do-clean:
	$(RM) -rf $(topdir)/class/lib/$(PROFILE)
