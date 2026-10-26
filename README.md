local ReplicatedStorage = game:GetService("ReplicatedStorage")

local function summonUnit(times)
    local summonEvent = ReplicatedStorage:FindFirstChild("Summon", true)
    if summonEvent then
        for i = 1, times do
            summonEvent:FireServer()
            task.wait(0.5)
        end
    end
end
