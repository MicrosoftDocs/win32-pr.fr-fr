---
description: Il existe plusieurs classes WMI et un objet de script pour analyser ou convertir le format DateTime CIM. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: dd01a732-5c88-4c24-a551-4d5452e712cc
ms.tgt_platform: multiple
title: 'Tâches WMI : dates et heures'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8864deb4f76b8ce6b76017c0348cdb86bf38b697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529431"
---
# <a name="wmi-tasks-dates-and-times"></a><span data-ttu-id="6ddd6-104">Tâches WMI : dates et heures</span><span class="sxs-lookup"><span data-stu-id="6ddd6-104">WMI Tasks: Dates and Times</span></span>

<span data-ttu-id="6ddd6-105">Il existe plusieurs classes WMI et un objet de script pour analyser ou convertir le format [DateTime CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-105">There are several WMI classes and a scripting object to parse or convert the [CIM datetime](date-and-time-format.md) format.</span></span> <span data-ttu-id="6ddd6-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="6ddd6-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="6ddd6-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="6ddd6-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="6ddd6-109">Pour exécuter un script</span><span class="sxs-lookup"><span data-stu-id="6ddd6-109">To run a script</span></span>

<span data-ttu-id="6ddd6-110">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="6ddd6-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="6ddd6-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="6ddd6-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="6ddd6-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="6ddd6-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="6ddd6-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="6ddd6-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="6ddd6-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="6ddd6-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="6ddd6-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="6ddd6-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="6ddd6-121">How do I...</span></span></th>
<th><span data-ttu-id="6ddd6-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="6ddd6-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ddd6-123">... convertir les dates WMI en dates et heures standard ?</span><span class="sxs-lookup"><span data-stu-id="6ddd6-123">...convert WMI dates to standard dates and times?</span></span><br/></td>
<td><span data-ttu-id="6ddd6-124">Utilisez l’objet <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> pour les convertir en dates et heures régulières.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-124">Use the <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> object to convert these to regular dates and times.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-125">VB</span><span class="sxs-lookup"><span data-stu-id="6ddd6-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Set dtmInstallDate = CreateObject(&quot;WbemScripting.SWbemDateTime&quot;)
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objOS = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each strOS in objOS
    dtmInstallDate.Value = strOS.InstallDate
    Wscript.Echo dtmInstallDate.GetVarDate
Next</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="6ddd6-126">Ou faire en sorte que votre code effectue la tâche manuellement.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-126">Or have your code do the task manually.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-127">VB</span><span class="sxs-lookup"><span data-stu-id="6ddd6-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Function WMIDateStringToDate(dtmInstallDate) 
    WMIDateStringToDate = CDate(Mid(dtmInstallDate, 5, 2) & &quot;/&quot; & Mid(dtmInstallDate, 7, 2) _
                        & &quot;/&quot; & Left(dtmInstallDate, 4) & &quot; &quot; & Mid (dtmInstallDate, 9, 2) & &quot;:&quot; _
                        & Mid(dtmInstallDate, 11, 2) & &quot;:&quot; & Mid(dtmInstallDate,13, 2)) 
End Function </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ddd6-128">... déterminer l’heure actuellement configurée sur un ordinateur ?</span><span class="sxs-lookup"><span data-stu-id="6ddd6-128">...determine the time currently configured on a computer?</span></span></p></td>
<td><p><span data-ttu-id="6ddd6-129">Utilisez la classe <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-129">Use the <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-130">VB</span><span class="sxs-lookup"><span data-stu-id="6ddd6-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_LocalTime&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Day:           &quot; & objItem.Day & VBNewLine _
               & &quot;Day Of Week:   &quot; & objItem.DayOfWeek & VBNewLine _
               & &quot;Hour:          &quot; & objItem.Hour & VBNewLine _
               & &quot;Minute:        &quot; & objItem.Minute & VBNewLine _
               & &quot;Month:         &quot; & objItem.Month & VBNewLine _
               & &quot;Quarter:       &quot; & objItem.Quarter & VBNewLine _
               & &quot;Second:        &quot; & objItem.Second & VBNewLine _
               & &quot;Week In Month: &quot; & objItem.WeekInMonth & VBNewLine _
               & &quot;Year:          &quot; & objItem.Year 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ddd6-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Specify computer and get Local Time
$Computer = &quot;.&quot;
$times = Get-WmiObject Win32_LocalTime -computer $computer

<# Now display the result #>

Foreach ($time in $times) {
    &quot;Day : {0}&quot; -f $Time.Day
    &quot;Day Of Week : {0}&quot; -f $Time.DayOfWeek
    &quot;Hour : {0}&quot; -f $Time.Hour
    &quot;Minute : {0}&quot; -f $Time.Minute
    &quot;Month : {0}&quot; -f $Time.Month
    &quot;Quarter : {0}&quot; -f $Time.Quarter
    &quot;Second : {0}&quot; -f $time.Second 
    &quot;Week In Month: {0}&quot; -f $Time.WeekInMonth 
    &quot;Year : {0}&quot; -f $Time.Year 
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ddd6-132">... déterminer le nom du fuseau horaire dans lequel un ordinateur est en cours d’exécution ?</span><span class="sxs-lookup"><span data-stu-id="6ddd6-132">...determine the name of the time zone in which a computer is running?</span></span></p></td>
<td><p><span data-ttu-id="6ddd6-133">Utilisez la classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> et vérifiez la valeur de la propriété <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class and check the value of the <strong>Description</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-134">VB</span><span class="sxs-lookup"><span data-stu-id="6ddd6-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TimeZone&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description:   &quot; & objItem.Description
    Wscript.Echo &quot;Daylight Name: &quot; & objItem.DaylightName
    Wscript.Echo &quot;Standard Name: &quot; & objItem.StandardName
    Wscript.Echo
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ddd6-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;  
$timezone = Get-WMIObject -class Win32_TimeZone -ComputerName $computer  
  
<# Display details  #>
if ($computer -eq &quot;.&quot;) {$computer = Hostname}  
&quot;Time zone information on computer `&quot;{0}`&quot;&quot; -f $computer  
&quot;Time Zone Description   : {0}&quot; -f $timezone.Description  
&quot;Daylight Name           : {0}&quot; -f $timezone.DaylightName  
&quot;Standard Name           : {0}&quot; -f $timezone.StandardName  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ddd6-136">... s’assurer que &quot; 10/02/2000 &quot; est interprété comme oct. 2, 2000, et non pas &quot; 10 fév, 2000 &quot; ?</span><span class="sxs-lookup"><span data-stu-id="6ddd6-136">...ensure that &quot;10/02/2000&quot; is interpreted as Oct. 2, 2000, not &quot;10 Feb, 2000&quot;?</span></span></p></td>
<td><p><span data-ttu-id="6ddd6-137">Gérez les dates au format <a href="datetime.md">DateTime</a> <a href="gloss-c.md"><em>CIM</em></a> et utilisez des méthodes <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> , telles que <a href="swbemdatetime-getvardate.md"><strong>getVarDate,</strong></a> , pour les convertir vers et depuis les formats <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a> ou <strong>VT_Date</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-137">Manage dates in <a href="gloss-c.md"><em>CIM</em></a> <a href="datetime.md">DATETIME</a> format and use <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> methods, such as <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> to convert to them to and from either <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> or <strong>VT_Date</strong> formats.</span></span> <span data-ttu-id="6ddd6-138">Étant donné que le format DATETIME est indépendant des paramètres régionaux, vous pouvez écrire un script qui s’exécute sur n’importe quel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-138">Because DATETIME format is locale-independent, you can write a script that runs on any machine.</span></span> <span data-ttu-id="6ddd6-139">Utilisez l’objet <strong>SWbemDateTime</strong> pour les convertir en dates et heures régulières.</span><span class="sxs-lookup"><span data-stu-id="6ddd6-139">Use the <strong>SWbemDateTime</strong> object to convert these to regular dates and times.</span></span> <span data-ttu-id="6ddd6-140">Pour plus d’informations sur la conversion de dates et d’heures, consultez <a href="date-and-time-format.md">format de date et d’heure</a> .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-140">See <a href="date-and-time-format.md">Date and Time Format</a> for more information on converting dates and times.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ddd6-141">... convertir un DateTime WMI en valeur DateTime .NET ?</span><span class="sxs-lookup"><span data-stu-id="6ddd6-141">...convert a WMI datetime to a .NET DateTime value?</span></span></p></td>
<td><p><span data-ttu-id="6ddd6-142">Analysez manuellement la chaîne, puis placez les valeurs récupérées dans un objet <a href="/dotnet/api/system.datetime">DateTime</a> .</span><span class="sxs-lookup"><span data-stu-id="6ddd6-142">Manually parse the string, then put the retrieved values into a <a href="/dotnet/api/system.datetime">DateTime</a> object.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd6-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ddd6-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDateTime( [String] $strWmiDate ) 
{ 
    $strWmiDate.Trim() > $null 
    $iYear   = [Int32]::Parse($strWmiDate.SubString( 0, 4)) 
    $iMonth  = [Int32]::Parse($strWmiDate.SubString( 4, 2)) 
    $iDay    = [Int32]::Parse($strWmiDate.SubString( 6, 2)) 
    $iHour   = [Int32]::Parse($strWmiDate.SubString( 8, 2)) 
    $iMinute = [Int32]::Parse($strWmiDate.SubString(10, 2)) 
    $iSecond = [Int32]::Parse($strWmiDate.SubString(12, 2)) 
<# decimal point is at $strWmiDate.Substring(14, 1) #> 
    $iMicroseconds = [Int32]::Parse($strWmiDate.Substring(15, 6)) 
    $iMilliseconds = $iMicroseconds / 1000 
    $iUtcOffsetMinutes = [Int32]::Parse($strWmiDate.Substring(21, 4)) 
    if ( $iUtcOffsetMinutes -ne 0 ) 
    { 
        $dtkind = [DateTimeKind]::Local 
    } 
    else 
    { 
        $dtkind = [DateTimeKind]::Utc 
    } 
    return New-Object -TypeName DateTime ` 
                      -ArgumentList $iYear, $iMonth, $iDay, ` 
                                    $iHour, $iMinute, $iSecond, ` 
                                    $iMilliseconds, $dtkind 
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6ddd6-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ddd6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ddd6-145">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="6ddd6-145">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="6ddd6-146">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="6ddd6-146">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="6ddd6-147">Format de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="6ddd6-147">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="6ddd6-148">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="6ddd6-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
