---
title: Fichiers d’espace réservé
description: Fichiers d’espace réservé
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "106531607"
---
# <a name="placeholder-files"></a>Fichiers d’espace réservé

## <a name="platform"></a>Plateforme

**Clients-** Windows 8.1  
**Serveurs-** Windows Server 2012 R2  

## <a name="description"></a>Description

Les fichiers d’espace réservé permettent aux utilisateurs d’afficher et de gérer les fichiers Microsoft OneDrive, quelle que soit la connectivité. Les fichiers d’espace réservé représentent l’espace de noms OneDrive, même lorsque les fichiers ne sont pas mis en cache localement. Ils contiennent des métadonnées de fichier et des images miniatures de photos.

## <a name="manifestation"></a>Manifestation

Pour les utilisateurs finaux et les développeurs, les fichiers d’espace réservé s’affichent et se comportent quasiment de la même façon que les fichiers locaux.

Si votre application utilise la boîte de dialogue de fichier commune pour énumérer le système de fichiers, votre application n’est pas affectée. Quand l’utilisateur tente d’ouvrir le fichier à partir de la boîte de dialogue commune/file, le contenu du fichier est téléchargé et est transmis à votre application.

Si votre application accède directement au système de fichiers, votre application peut tirer parti des fichiers d’espace réservé à l’aide des instructions ci-dessous.

## <a name="solution"></a>Solution

-   Les espaces réservés sont masqués par Convention en fonction des attributs
-   Identifier les espaces réservés à l’aide de la balise d’analyse ID d’analyse d’analyse d’e/s \_ \_ \_ \_

Utilisez le modèle de données Shell pour un comportement transparent :

-   Utiliser SHCreateItemFromParsingName () pour créer un élément de Shell
-   Liaison au flux à l’aide de IShellItem :: BindToHandler (BHID \_ Stream)
-   Gestionnaire de propriétés utilisateur pour l’accès aux propriétés (IShellItem2 :: GetPropertyHandler)
-   Thumbnailhandler de l’interface utilisateur pour obtenir des images miniatures pour les espaces réservés
-   Spécifiez SupportedProtocols = \* sur votre implémentation de verbe si le verbe est lié au flux via BindToHandler


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




