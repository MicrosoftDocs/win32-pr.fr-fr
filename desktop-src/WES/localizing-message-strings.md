---
title: Localiser des chaînes de message
description: Chaque chaîne de message que vous spécifiez dans le manifeste doit faire référence à une chaîne dans la section localisation du manifeste.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031541"
---
# <a name="localizing-message-strings"></a><span data-ttu-id="2fa13-103">Localiser des chaînes de message</span><span class="sxs-lookup"><span data-stu-id="2fa13-103">Localizing Message Strings</span></span>

<span data-ttu-id="2fa13-104">Chaque chaîne de message que vous spécifiez dans le manifeste doit faire référence à une chaîne dans la section **localisation** du manifeste.</span><span class="sxs-lookup"><span data-stu-id="2fa13-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="2fa13-105">La section localization contient une section de table de chaînes pour chaque paramètre régional que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="2fa13-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="2fa13-106">L’exemple suivant montre comment définir une table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="2fa13-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="2fa13-107">Vous devez spécifier les attributs **ID** et **value** de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2fa13-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="2fa13-108">Vous utilisez la valeur de l’attribut **ID** pour référencer la chaîne dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="2fa13-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="2fa13-109">L’attribut **value** contient la chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="2fa13-109">The **value** attribute contains the localized string.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


<span data-ttu-id="2fa13-110">Au lieu d’ajouter des chaînes localisées au manifeste, vous devez créer un fichier d’interface utilisateur multilingue (MUI) pour chaque langue que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="2fa13-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="2fa13-111">Utilisez un fichier texte de message pour spécifier vos chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="2fa13-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="2fa13-112">La procédure suivante décrit comment créer un fichier MUI pour l’anglais et le français.</span><span class="sxs-lookup"><span data-stu-id="2fa13-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="2fa13-113">**Pour créer un fichier MUI pour l’anglais et le français**</span><span class="sxs-lookup"><span data-stu-id="2fa13-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="2fa13-114">Créez un fichier texte de message qui crée les chaînes de message en français.</span><span class="sxs-lookup"><span data-stu-id="2fa13-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="2fa13-115">Pour plus d’informations sur la création d’un fichier texte de message, consultez [fichiers texte du message](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="2fa13-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="2fa13-116">Les identificateurs de message que vous spécifiez dans le fichier texte du message doivent correspondre aux identificateurs de ressource générés par le compilateur de message pour les mêmes chaînes dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="2fa13-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="2fa13-117">Pour déterminer les identificateurs de ressource utilisés pour les chaînes dans le manifeste, consultez le fichier. h que le compilateur de messages a généré lorsque vous avez compilé le manifeste.</span><span class="sxs-lookup"><span data-stu-id="2fa13-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  <span data-ttu-id="2fa13-118">Exécutez les commandes suivantes pour créer la DLL de ressource qui contient vos chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="2fa13-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="2fa13-119">Le fichier messages.mc est le fichier texte du message que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="2fa13-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="2fa13-120">Dans le dossier qui contient votre fournisseur, créez un sous-dossier pour chaque paramètre régional que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="2fa13-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="2fa13-121">Le nom du sous-dossier doit être le nom de la langue pour ces paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2fa13-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="2fa13-122">Par exemple, pour 0x0409, utilisez en-US comme nom de dossier.</span><span class="sxs-lookup"><span data-stu-id="2fa13-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="2fa13-123">Créez un fichier. rcconfig qui indique à l’outil Muirct.exe que vous souhaitez fractionner les ressources de chaîne de message de l’exécutable et des dll de ressource.</span><span class="sxs-lookup"><span data-stu-id="2fa13-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="2fa13-124">Voici un exemple de fichier. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="2fa13-124">The following is an example .rcconfig file.</span></span>
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  <span data-ttu-id="2fa13-125">Exécutez les commandes de Muirct.exe suivantes pour fractionner les chaînes en anglais du fichier exécutable du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2fa13-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="2fa13-126">Exécutez les commandes de Muirct.exe suivantes pour fractionner les chaînes françaises de la DLL de ressource.</span><span class="sxs-lookup"><span data-stu-id="2fa13-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="2fa13-127">Supprimez le fichier indépendant de la langue (fr-FR \\messages.dll) après la création du fichier MUI.</span><span class="sxs-lookup"><span data-stu-id="2fa13-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="2fa13-128">Renommez provider.exe. ln en provider.exe.</span><span class="sxs-lookup"><span data-stu-id="2fa13-128">Rename provider.exe.ln to provider.exe.</span></span>