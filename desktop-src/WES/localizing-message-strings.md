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
# <a name="localizing-message-strings"></a>Localiser des chaînes de message

Chaque chaîne de message que vous spécifiez dans le manifeste doit faire référence à une chaîne dans la section **localisation** du manifeste. La section localization contient une section de table de chaînes pour chaque paramètre régional que vous prenez en charge.

L’exemple suivant montre comment définir une table de chaînes. Vous devez spécifier les attributs **ID** et **value** de la chaîne. Vous utilisez la valeur de l’attribut **ID** pour référencer la chaîne dans votre manifeste. L’attribut **value** contient la chaîne localisée.


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


Au lieu d’ajouter des chaînes localisées au manifeste, vous devez créer un fichier d’interface utilisateur multilingue (MUI) pour chaque langue que vous prenez en charge. Utilisez un fichier texte de message pour spécifier vos chaînes localisées.

La procédure suivante décrit comment créer un fichier MUI pour l’anglais et le français.

**Pour créer un fichier MUI pour l’anglais et le français**

1.  Créez un fichier texte de message qui crée les chaînes de message en français. Pour plus d’informations sur la création d’un fichier texte de message, consultez [fichiers texte du message](/windows/desktop/EventLog/message-text-files). Les identificateurs de message que vous spécifiez dans le fichier texte du message doivent correspondre aux identificateurs de ressource générés par le compilateur de message pour les mêmes chaînes dans le manifeste. Pour déterminer les identificateurs de ressource utilisés pour les chaînes dans le manifeste, consultez le fichier. h que le compilateur de messages a généré lorsque vous avez compilé le manifeste.
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


2.  Exécutez les commandes suivantes pour créer la DLL de ressource qui contient vos chaînes localisées. Le fichier messages.mc est le fichier texte du message que vous avez créé à l’étape 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Dans le dossier qui contient votre fournisseur, créez un sous-dossier pour chaque paramètre régional que vous prenez en charge. Le nom du sous-dossier doit être le nom de la langue pour ces paramètres régionaux. Par exemple, pour 0x0409, utilisez en-US comme nom de dossier.
4.  Créez un fichier. rcconfig qui indique à l’outil Muirct.exe que vous souhaitez fractionner les ressources de chaîne de message de l’exécutable et des dll de ressource. Voici un exemple de fichier. rcconfig.
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
  

5.  Exécutez les commandes de Muirct.exe suivantes pour fractionner les chaînes en anglais du fichier exécutable du fournisseur.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Exécutez les commandes de Muirct.exe suivantes pour fractionner les chaînes françaises de la DLL de ressource. Supprimez le fichier indépendant de la langue (fr-FR \\messages.dll) après la création du fichier MUI.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Renommez provider.exe. ln en provider.exe.