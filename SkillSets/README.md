The CSV file contains the list of Skills exported from Security copilot
YOu can run the following KQL query to see the list inside Sentinel/Log Analytics:

externaldata (PluginName:string, SkillName:string, SkillDescription:string) [@"https://raw.githubusercontent.com/jguimera/SecurityCopilot/refs/heads/main/SkillSets/SecurityCopilotSkills.csv"] with (format="csv",ignoreFirstRecord=true)
