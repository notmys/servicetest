-- All Services Working For Executors
-- By Mys (01xMYS) ❤️
local function GetService(serviceName)
    local success, result = pcall(game.GetService, game, serviceName)
    
    if success and result then
        return result
    else
        return nil
    end
end

local services = {
    'Workspace', 'GuiService', 'Stats', 'TimerService', 'SoundService', 'VideoCaptureService', 'LogService',
    'ContentProvider', 'KeyframeSequenceProvider', 'AnimationClipProvider', 'Chat', 'MarketplaceService', 'Players',
    'PointsService', 'NotificationService', 'ReplicatedFirst', 'HttpRbxApiService', 'TweenService', 'MaterialService',
    'TextChatService', 'TextService', 'PlayerEmulatorService', 'CorePackages', 'StudioData', 'SharedTableRegistry',
    'StarterPlayer', 'StarterPack', 'StarterGui', 'CoreGui', 'LocalizationService', 'PolicyService', 'JointsService',
    'CollectionService', 'PhysicsService', 'BadgeService', 'GeometryService', 'FriendService', 'InsertService',
    'GamePassService', 'Debris', 'CookiesService', 'Selection', 'UserInputService', 'KeyboardService', 'MouseService',
    'VRService', 'ContextActionService', 'ScriptService', 'AssetService', 'TouchInputService', 'BrowserService',
    'CaptureService', 'AppStorageService', 'AnalyticsService', 'HeatmapService', 'RbxAnalyticsService', 'HttpService',
    'Lighting', 'ThirdPartyUserService', 'PlatformFriendsService', 'PlatformCloudStorageService', 'GenericChallengeService',
    'ScriptRegistrationService', 'RuntimeScriptService', 'RobloxReplicatedStorage', 'MessageBusService', 'MemStorageService',
    'IXPService', 'ChangeHistoryService', 'ExperienceStateCaptureService', 'GamepadService', 'MeshContentProvider',
    'SolidModelContentProvider', 'HSRDataContentProvider', 'VideoService', 'TextBoxService', 'ControllerService',
    'EventIngestService', 'WebViewService', 'LinkingService', 'HapticService', 'UIDragDetectorService', 'NetworkClient',
    'VoiceChatService', 'Visit', 'GuidRegistryService', 'PermissionsService', 'Teams', 'FeatureRestrictionManager',
    'ExperienceAuthService', 'CommerceService', 'ReplicatedStorage', 'TestService', 'AdService', 'SocialService',
    'SafetyService', 'ProximityPromptService', 'AvatarChatService', 'FacialAnimationStreamingServiceV2', 'AvatarCreationService',
    'GenerationService', 'RobloxServerStorage', 'ScriptProfilerService', 'HeapProfilerService', 'TelemetryService',
    'SessionService', 'ExperienceService', 'AudioFocusService', 'UserService', 'FaceAnimatorService', 'GroupService',
    'AccountService', 'OmniRecommendationsService', 'DataModelPatchService', 'MessagingService', 'AvatarEditorService',
    'AppUpdateService', 'CreatorStoreService', 'RtMessagingService', 'ExperienceNotificationService', 'AchievementService',
    'PlayerViewService', 'SpawnerService', 'VoiceChatInternal', 'TextChatService', 'GameSettingsService', 'AvatarService',
    'SocialFriendsService', 'ScriptableXFileService', 'SurfaceGuiService', 'LocalizationAppService', 'CrossGameStoreService',
    'AnalyticsAppService', 'PostProcessService', 'RobloxGui', 'NetworkServer', 'VoxelsService', 'MathService',
    'BedwarsService', 'AdStudioService', 'PhysicsNetworkService', 'CollectionServiceV2', 'AvatarSubService'
}

local successfulServices = {}
local failedServices = {}

for _, serviceName in ipairs(services) do
    local service = GetService(serviceName)
    if service then
        successfulServices[#successfulServices + 1] = serviceName
    else
        failedServices[#failedServices + 1] = serviceName
    end
end

print(("\nSuccessfully Loaded (%d/%d):"):format(#successfulServices, #services))
for _, serviceName in ipairs(successfulServices) do
    print("✅ " .. serviceName)
end

print(("\nFailed to Load (%d/%d):"):format(#failedServices, #services))
for _, serviceName in ipairs(failedServices) do
    print("❌ " .. serviceName)
end
