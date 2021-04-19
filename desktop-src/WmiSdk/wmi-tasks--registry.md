---
description: Les tâches WMI pour le registre créent et modifient des clés et des valeurs de registre. Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'Tâches WMI : Registre'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526217"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="f9a2c-104">Tâches WMI : Registre</span><span class="sxs-lookup"><span data-stu-id="f9a2c-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="f9a2c-105">Les tâches WMI pour le registre créent et modifient des clés et des valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="f9a2c-106">Pour obtenir d’autres exemples, consultez le site TechNet ScriptCenter à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="f9a2c-107">Les exemples de scripts présentés dans cette rubrique obtiennent des données uniquement à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f9a2c-108">Pour plus d’informations sur l’utilisation du script pour obtenir des données à partir d’ordinateurs distants, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f9a2c-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f9a2c-109">La procédure suivante décrit comment exécuter un script.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f9a2c-110">**Pour exécuter un script**</span><span class="sxs-lookup"><span data-stu-id="f9a2c-110">**To run a script**</span></span>

1.  <span data-ttu-id="f9a2c-111">Copiez le code et enregistrez-le dans un fichier avec une extension. vbs, par exemple *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f9a2c-112">Assurez-vous que votre éditeur de texte n’ajoute pas d’extension. txt au fichier.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f9a2c-113">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire où vous avez enregistré le fichier.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f9a2c-114">Tapez **cscript filename.vbs** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f9a2c-115">Si vous ne pouvez pas accéder à un journal des événements, vérifiez si vous exécutez à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f9a2c-116">Certains journaux des événements, tels que le journal des événements de sécurité, peuvent être protégés par les contrôles d’accès utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="f9a2c-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f9a2c-117">Par défaut, cscript affiche la sortie d’un script dans la fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f9a2c-118">Étant donné que les scripts WMI peuvent générer de grandes quantités de sortie, vous souhaiterez peut-être rediriger la sortie vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f9a2c-119">Tapez **cscript filename.vbs > outfile.txt** à l’invite de commandes pour rediriger la sortie du script *filename.vbs* vers *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="f9a2c-120">Le tableau suivant répertorie des exemples de scripts qui peuvent être utilisés pour obtenir différents types de données à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-121">Comment puis-je...</span><span class="sxs-lookup"><span data-stu-id="f9a2c-121">How do I...</span></span></th>
<th><span data-ttu-id="f9a2c-122">Classes ou méthodes WMI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a2c-123">... lire les valeurs de clé de Registre à l’aide de WMI ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="f9a2c-124">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="f9a2c-125">Vous ne pouvez obtenir aucune instance de cette classe, car le <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">fournisseur de Registre système</a> est une méthode et un fournisseur d’événements uniquement.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="f9a2c-126">Toutefois, vous pouvez récupérer des données de Registre par le biais de méthodes telles que <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>enumKey</strong></a> ou <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="f9a2c-127">Le <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, situé dans l’espace de noms root\cimv2, obtient des données sur le registre dans son ensemble, par exemple sa taille.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-128">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a2c-130">... créer une nouvelle clé de Registre ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="f9a2c-131">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default, et la méthode <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-132">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a2c-134">... créer une valeur de Registre sous une clé ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="f9a2c-135">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default, et la méthode <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="f9a2c-136">Utilisez ensuite l’une des méthodes Set, en fonction du type de données de registre dont la valeur est, par exemple <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="f9a2c-137">Les méthodes Set créent une valeur si elle n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="f9a2c-138">Pour plus d’informations, consultez <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mappage d’un type de données de Registre à un type de données WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-139">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a2c-141">... éviter d’obtenir une erreur de classe non valide lors de la tentative d’écriture d’un script pour lire le registre ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="f9a2c-142">Utilisez l’espace de noms root\default lors de l’accès à la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="f9a2c-143"><strong>StdRegProv</strong> ne fait pas partie de l’espace de noms CIMV2, ce qui explique pourquoi une &quot; erreur de classe non valide &quot; est générée si vous essayez de vous connecter à &quot; root\cimv2 : StdRegProv &quot; .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-144">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a2c-145">... vérifier la sécurité sur une clé de Registre spécifique ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="f9a2c-146">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default et la méthode <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="f9a2c-147">Vous pouvez uniquement vérifier les droits d’accès de l’utilisateur actuel qui exécute le script ou l’application.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="f9a2c-148">Vous ne pouvez pas vérifier les droits d’accès d’un autre utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a2c-149">... lire et écrire des valeurs de Registre binaires ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="f9a2c-150">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans &quot; &quot; l’espace de noms Root\Default et les méthodes <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>getBinaryValue</strong></a> et <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="f9a2c-151">Les valeurs de Registre qui s’affichent dans l’utilitaire RegEdt32 sous la forme d’une série de valeurs hexadécimales d’octet sont au format de données <strong>REG_BINARY</strong> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="f9a2c-152">Pour plus d’informations, consultez <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mappage d’un type de données de Registre à un type de données WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="f9a2c-153">L’exemple de code VBScript suivant crée une clé avec une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="f9a2c-154">La valeur binaire est fournie dans le tableau d’octets <em>iValues</em> spécifié au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-155">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="f9a2c-156">Le script suivant lit la valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-157">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a2c-159">... lire et écrire des valeurs de Registre qui contiennent plusieurs chaînes ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="f9a2c-160">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default et les méthodes <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> et <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="f9a2c-161">Les clés de Registre qui s’affichent dans l’utilitaire RegEdt32 sous la forme d’une série de chaînes séparées par des espaces sont au format de données <strong>REG_MULTI_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="f9a2c-162">Pour plus d’informations, consultez <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mappage d’un type de données de Registre à un type de données WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="f9a2c-163">L’exemple de code VBScript suivant crée une nouvelle clé et une nouvelle valeur multichaîne.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-164">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="f9a2c-166">Le script suivant lit la valeur multichaîne.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-167">VB</span><span class="sxs-lookup"><span data-stu-id="f9a2c-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a2c-169">... supprimer une clé de Registre ?</span><span class="sxs-lookup"><span data-stu-id="f9a2c-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="f9a2c-170">Utilisez la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , située dans l’espace de noms root\default et les méthodes <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9a2c-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9a2c-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f9a2c-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9a2c-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a2c-173">Tâches WMI pour les scripts et les applications</span><span class="sxs-lookup"><span data-stu-id="f9a2c-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f9a2c-174">Exemples d’applications WMI C++</span><span class="sxs-lookup"><span data-stu-id="f9a2c-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f9a2c-175">ScriptCenter TechNet</span><span class="sxs-lookup"><span data-stu-id="f9a2c-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="f9a2c-176">Modification du Registre système</span><span class="sxs-lookup"><span data-stu-id="f9a2c-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="f9a2c-177">**StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="f9a2c-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
