---
description: Vous pouvez utiliser la bibliothèque de types de scripts WMI pour appeler les méthodes de l’API de script WMI à partir de Microsoft Visual Studio et dans les fichiers Windows Script Host WSF.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Utilisation de la bibliothèque de types de scripts WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541881"
---
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="47eb9-103">Utilisation de la bibliothèque de types de scripts WMI</span><span class="sxs-lookup"><span data-stu-id="47eb9-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="47eb9-104">Vous pouvez utiliser la bibliothèque de types de scripts WMI pour appeler les méthodes de l’API de script WMI à partir de Microsoft Visual Studio et dans les fichiers Windows Script Host WSF.</span><span class="sxs-lookup"><span data-stu-id="47eb9-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="47eb9-105">Utilisation de la bibliothèque de types de scripts WMI avec Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="47eb9-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="47eb9-106">Les fonctionnalités de Visual InterDev 6,0 ont été intégrées à [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="47eb9-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="47eb9-107">La procédure suivante décrit comment permettre à l’environnement de développement intégré (IDE) d’être conscient de la bibliothèque de types WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="47eb9-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="47eb9-108">**Pour ajouter la bibliothèque de types de scripts WMI aux références de projet**</span><span class="sxs-lookup"><span data-stu-id="47eb9-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="47eb9-109">Sélectionnez **Ajouter des références** dans le menu **projet** .</span><span class="sxs-lookup"><span data-stu-id="47eb9-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="47eb9-110">Dans l’onglet COM de la zone **Ajouter une référence** , sélectionnez Bibliothèque de scripts Microsoft WMI v 1.2.</span><span class="sxs-lookup"><span data-stu-id="47eb9-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="47eb9-111">Si aucune option appropriée n’apparaît dans la liste Références, ajoutez-la à l’aide de l’option **Parcourir** dans la zone **références** .</span><span class="sxs-lookup"><span data-stu-id="47eb9-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="47eb9-112">L' **exploration** ouvre une zone **Ajouter une référence** qui vous permet de rechercher la bibliothèque de types WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="47eb9-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="47eb9-113">La bibliothèque de types WbemScripting réside dans le fichier wbemdisp. tlb dans le répertoire% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="47eb9-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="47eb9-114">Sélectionnez le fichier et cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="47eb9-114">Select the file and click **Open**.</span></span> <span data-ttu-id="47eb9-115">La bibliothèque Microsoft WMI Scripting V 1.2 apparaît dans la liste des références.</span><span class="sxs-lookup"><span data-stu-id="47eb9-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="47eb9-116">Veillez à activer la case à cocher en regard de cet élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="47eb9-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="47eb9-117">Utilisation de la bibliothèque de types de scripts WMI avec Windows Script Host 2,0</span><span class="sxs-lookup"><span data-stu-id="47eb9-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="47eb9-118">Vous pouvez inclure la référence à **WbemScripting. SWbemLocator** dans un fichier Windows Script Host wsf, contrairement à un script écrit dans Visual Basic, l’édition de script ou d’autres langages de script.</span><span class="sxs-lookup"><span data-stu-id="47eb9-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="47eb9-119">Cela vous permet d’utiliser des noms de constantes au lieu de valeurs.</span><span class="sxs-lookup"><span data-stu-id="47eb9-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="47eb9-120">Par exemple, utilisez **WbemAuthenticationLevelPktPrivacy** plutôt que la valeur 6 lors de la définition de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="47eb9-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="47eb9-121">Les scripts peuvent se connecter à l’API de script pour la bibliothèque de types WMI à l’aide des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="47eb9-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="47eb9-122">Spécification du GUID WbemScripting dans les méthodes VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) et [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="47eb9-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="47eb9-123">Cela alerte Windows Script Host pour se connecter au jeu d’objets WMI.</span><span class="sxs-lookup"><span data-stu-id="47eb9-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="47eb9-124">L’exemple de code VBScript suivant crée un nouvel objet [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="47eb9-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="47eb9-125">Utilisation de la [chaîne de moniker](constructing-a-moniker-string.md) « winmgmts : » lors de l’obtention d’un objet nouveau ou existant.</span><span class="sxs-lookup"><span data-stu-id="47eb9-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="47eb9-126">L’exemple de code VBScript suivant utilise le moniker « winmgmts : » pour obtenir l’instance [**du \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) avec une propriété **handle** égale à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="47eb9-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="47eb9-127">**Descripteur** est la propriété de clé pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="47eb9-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="47eb9-128">Référencement de la bibliothèque de types WMI à l’aide <reference> de la balise du format de fichier XML WSH 2,0.</span><span class="sxs-lookup"><span data-stu-id="47eb9-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="47eb9-129">Si vous utilisez la <reference> balise, la balise doit avoir soit un attribut **UUID** dont la valeur est le **GUID** de la bibliothèque de types WMI, soit (recommandé) un attribut d’objet dont la valeur est le **ProgID** de l’un des objets de script WMI que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="47eb9-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="47eb9-130">L’exemple de code VBScript suivant utilise le PROGID « WbemScripting ».</span><span class="sxs-lookup"><span data-stu-id="47eb9-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="47eb9-131">Pour exécuter le script, enregistrez le texte dans un fichier avec une extension. wsf.</span><span class="sxs-lookup"><span data-stu-id="47eb9-131">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   <span data-ttu-id="47eb9-132">Utilisation d’une balise d'> **objet** <pour créer un objet de script WMI.</span><span class="sxs-lookup"><span data-stu-id="47eb9-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="47eb9-133">Vous pouvez spécifier l’attribut **ID** avec la valeur d’un nom qui fait référence à l’objet de script WMI que vous souhaitez créer, et l’attribut **ProgID** égal à PROID de l’objet de script WMI.</span><span class="sxs-lookup"><span data-stu-id="47eb9-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="47eb9-134">Le script WSH suivant affiche le nom d’hôte et le nombre de processeurs sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="47eb9-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="47eb9-135">Pour exécuter le script, enregistrez le texte dans un fichier avec une extension. wsf.</span><span class="sxs-lookup"><span data-stu-id="47eb9-135">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a><span data-ttu-id="47eb9-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47eb9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47eb9-137">Scripts dans WMI</span><span class="sxs-lookup"><span data-stu-id="47eb9-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="47eb9-138">API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="47eb9-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
