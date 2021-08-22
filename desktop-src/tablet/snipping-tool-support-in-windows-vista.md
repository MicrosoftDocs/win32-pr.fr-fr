---
description: Cette rubrique décrit comment votre application peut spécifier l’URL que l’outil capture de Tablet PC doit obtenir lors de la capture de votre application.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: prise en charge de l’outil capture dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2c24901524500df97461f3b3acf88d9a51f73cc24134955c1df866a457a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966768"
---
# <a name="snipping-tool-support-in-windows-vista"></a>prise en charge de l’outil capture dans Windows Vista

Cette rubrique décrit comment votre application peut spécifier l’URL que l’outil capture de Tablet PC doit obtenir lors de la capture de votre application.

## <a name="specifying-the-url-via-registry-key"></a>Spécification de l’URL via une clé de Registre

L’outil capture permet aux utilisateurs de capturer une capture (capture d’écran) de n’importe quel objet sur l’écran, puis d’annoter, d’enregistrer ou de partager l’image. Lorsque les données sont enregistrées au format HTML, ou lorsqu’elles sont envoyées à un client de messagerie qui prend en charge le code HTML Inline, l’outil capture peut ajouter une URL à la capture si l’application fournit des informations sur l’obtention de l’URL.

L’outil capture obtient l’URL via des objets d’accessibilité. Les applications doivent spécifier les informations nécessaires sous les clés de Registre suivantes :

HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC \\ capture Tool \\ LinkFingerprints,

Et doivent créer une sous-clé dont le nom est identique à celui de la classe de fenêtre à partir de laquelle le lien doit être obtenu. Le nom de la classe de fenêtre doit être la fenêtre de premier plan de l’application.

HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC \\ capture Tool \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Détails de la clé de classe de fenêtre

Sous la clé de la classe de fenêtre, les valeurs appropriées doivent être définies pour indiquer que l’outil capture doit détecter l’objet d’accessibilité correct.



| VALEUR                        | TYPE                  | FILTRAGE            | INFORMATIONS STOCKÉES                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | \_valeur DWORD reg<br/> |                 | Indique l’un des champs suivants à vérifier<br/> |
| Name<br/>              | SZ de REG \_<br/>    | 0x02<br/> | Nom de l’accessibilité<br/>                               |
| Description<br/>       | SZ de REG \_<br/>    | 0x04<br/> | Description de l’accessibilité<br/>                        |
| Role<br/>              | \_valeur DWORD reg<br/> | 0x08<br/> | Rôle d’accessibilité<br/>                               |
| ParentName<br/>        | SZ de REG \_<br/>    | 0x10<br/> | Nom d’accessibilité du parent<br/>                     |
| ParentValue<br/>       | SZ de REG \_<br/>    | 0x20<br/> | Valeur d’accessibilité du parent<br/>                    |
| ParentRole<br/>        | \_valeur DWORD reg<br/> | 0x40<br/> | Rôle d’accessibilité du parent<br/>                     |
| ParentDescription<br/> | SZ de REG \_<br/>    | 0x80<br/> | Description de l’accessibilité du parent<br/>              |



 

En outre, si la valeur de bit de masque 0x1 est définie, l’URL doit être extraite du nom d’accessibilité. dans le cas contraire, l’URL doit être extraite de la valeur d’accessibilité.

Si l’application utilise des chaînes localisées pour les \_ valeurs de Reg SZ ci-dessus, la chaîne doit être fournie en tant que chaîne indirecte en utilisant le format suivant :

@filename, ressource

La chaîne est extraite du fichier nommé, en utilisant la valeur de ressource en tant que localisateur. Si la valeur de ressource est égale ou supérieure à zéro, le nombre devient l’index de la chaîne dans le fichier binaire. Si le nombre est négatif, il devient un identificateur de ressource (ID).

> [!Note]  
> les constantes de rôle se trouvent dans oleacc. h dans le SDK Windows. les valeurs de registre décrites sont spécifiques à Windows Vista.

 

 

 




