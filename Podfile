use_frameworks!

source 'https://github.com/CocoaPods/Specs'
source 'https://github.com/PopcornTimeTV/Specs'

def pods
    pod 'PopcornTorrent', '~> 1.3.15'
    pod 'XCDYouTubeKit', '~> 2.12.0'
    pod 'Alamofire', '~> 5.1.0'
    pod 'AlamofireImage', '~> 4.1.0'
    pod 'SwiftyTimer', :git => 'https://github.com/radianttap/SwiftyTimer', :branch => 'swift5'
    pod 'Reachability', :git => 'https://github.com/tonymillion/Reachability'
    pod 'MarqueeLabel', '~> 4.0.2'
    pod 'ObjectMapper', '~> 3.5.2'
end

target 'PopcornTimeiOS' do
    platform :ios, '13.0'
    pods
    pod 'FloatRatingView', '~> 4.0'
    pod 'google-cast-sdk-no-bluetooth', '~> 4.4.7'
    pod 'OBSlider', '~> 1.1.1'
    pod 'MobileVLCKit', '~> 3.3.10'
end

target 'PopcornTimetvOS' do
    platform :tvos, '13.0'
    pods
    pod 'TvOSMoreButton', '~> 1.3.0'
    pod 'TVVLCKit', '~> 3.3.10'
    pod 'MBCircularProgressBar', '~> 0.3.5-1'
end

target 'TopShelf' do
    platform :tvos, '13.0'
    pod 'ObjectMapper', '~> 3.5.2'
end

def kitPods
    pod 'Alamofire', '~> 5.1.0'
    pod 'ObjectMapper', '~> 3.5.2'
    pod 'SwiftyJSON', '~> 5.0.0'
    pod 'Locksmith', '~> 4.0.0'
end

target 'PopcornKit tvOS' do
    platform :tvos, '13.0'
    kitPods
end

target 'PopcornKit iOS' do
    platform :ios, '13.0'
    kitPods
    pod 'google-cast-sdk-no-bluetooth', '~> 4.4.7'
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['EXPANDED_CODE_SIGN_IDENTITY'] = ""
            config.build_settings['CODE_SIGNING_REQUIRED'] = "NO"
            config.build_settings['CODE_SIGNING_ALLOWED'] = "NO"
        end
    end
end
