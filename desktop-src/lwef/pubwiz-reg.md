---
title: Inscription d’un service
description: pour ajouter votre service à la liste des fournisseurs dans l’assistant publication de sites Web ou l’assistant commande d’impression en ligne, vous devez ajouter la clé appropriée et ses valeurs au registre Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- inscription, services
- Assistant Publication de sites Web, inscription
- Assistant commande d’impression en ligne, inscription
- inscrire, Assistant Publication de sites Web
- inscrire, Assistant commande d’impression en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608639"
---
# <a name="registering-a-service"></a>Inscription d’un service

pour ajouter votre service à la liste des fournisseurs dans l’assistant publication de sites Web ou l’assistant commande d’impression en ligne, vous devez ajouter la clé appropriée et ses valeurs au registre Windows.

## <a name="required-keys-and-values"></a>Clés et valeurs requises

Pour ajouter votre service à la liste des fournisseurs de l’Assistant Publication de sites Web, ajoutez une clé comme indiqué ci-dessous.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Pour ajouter votre service à la liste des fournisseurs de l’Assistant commande d’impression en ligne, ajoutez une clé comme indiqué ci-dessous.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Chacune des valeurs est une chaîne de type REG \_ sz. Fournissez ses données comme expliqué dans le tableau suivant. 

| Nom de la valeur     | Explication                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Chemin d’accès complet au fichier d’icône, y compris le nom de fichier.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Nom affiché pour votre service dans la liste des fournisseurs de l’Assistant.                                                                                                                                                                                                                                                                                                                                                             |
| Description    | Brève description de votre service. Cette description s’affiche également dans la liste des fournisseurs de l’Assistant, directement sous le nom de votre service.                                                                                                                                                                                                                                                                                    |
| HREF           | URL de la première page de votre service.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Types de fichiers pris en charge par votre service. Par exemple, *\*.jpg*. En spécifiant uniquement certains types de fichiers, votre service s’affiche uniquement lorsque ces types de fichiers ont été sélectionnés. Si plusieurs types de fichier ont été sélectionnés, votre service s’affiche si l’un de ces types de fichiers est pris en charge par votre service. Si vous souhaitez spécifier plusieurs types de fichiers, séparez-les par des points-virgules dans la liste. Par exemple, *\*.jpg ; \*.bmp*. |



 

Voici un exemple complet pour un service de traitement des photos nommé « MyProvider ».

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Lorsque l’URL de votre service est appelée, deux valeurs sont ajoutées à la fin de l’URL : LCID et langid. Par exemple, la chaîne d’URL de l’exemple ci-dessus peut être https : \/ /www.MyProvider.com/Intro.htm ? LCID = 1033&LangID = 1033. Ces variables sont utilisées pour les informations de langue et de localisation.

-   **LCID** est utilisé pour informer le serveur des paramètres pays/région et langue du client. Elle n’est pas utilisée pour déterminer la langue de l’interface utilisateur du client, mais elle est utilisée pour déterminer le format approprié pour la devise, la date et l’heure, ainsi que pour d’autres données spécifiques à la région.
-   **LangID** est utilisé pour informer le serveur du paramètre de langue par défaut du client afin qu’il puisse utiliser la langue appropriée dans l’interface utilisateur.

 

 




