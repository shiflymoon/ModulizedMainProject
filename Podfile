# Uncomment this line to define a global platform for your project
# platform :ios, '9.0'

source 'https://github.com/ModulizationDemo/PrivatePods.git'
source 'https://github.com/CocoaPods/Specs.git'

#增加编译所有库为静态库方法，因为使用swift必须开启use_frameworks!
#swift使用其他oc模块，所以必须开启use_modular_headers!
#开启了use_frameworks!，所有库会自动编译为动态库，除非
#在podspec中设置s.static_framework = true，但是一般库都没有设置
#但可以通过如下语句解决（当然可以把别人的podspec 克隆到自己服务器，指定git来源，不推荐）

pre_install do |installer|

Pod::PodTarget.send(:define_method, :static_framework?) { return true }
end

target 'MainProject' do
  # Uncomment this line if you're using Swift or would like to use dynamic frameworks
  use_frameworks!
  use_modular_headers!
  #
  pod 'A_Category'
  pod 'A_Extension'
  pod 'HandyFrame'
  pod 'A'
  pod 'A_swift'
  pod 'CTMediator'

end
