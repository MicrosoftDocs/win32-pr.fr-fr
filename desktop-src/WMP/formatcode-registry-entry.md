---
title: Entrée de Registre FormatCode
description: Entrée de Registre FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Lecteur Windows Media, entrées de registre FormatCode
- Lecteur Windows Media, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées FormatCode
- registre, paramètres pour Lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Entrées de Registre FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120518"
---
# <a name="formatcode-registry-entry"></a>Entrée de Registre FormatCode

lorsque Lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de registre qui correspond à l’extension. la sous-clé est décrite dans la [Paramètres du registre](file-name-extension-registry-settings.md)de l’Extension de nom de fichier. L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **FormatCode** .

L’entrée de Registre **FormatCode** spécifie le code de format MTP (Media Transport Protocol) pour les fichiers qui ont l’extension personnalisée. L’entrée de Registre **FormatCode** se présente sous la forme suivante.



| Nom       | Type           | Valeur                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **\_valeur DWORD reg** | Entier positif 16 bits qui identifie le format du fichier. |



 

lorsque l’utilisateur tente de copier un fichier multimédia numérique ayant une extension de nom de fichier personnalisée sur un appareil mobile, Lecteur Windows Media recherche dans le registre un code de format associé à l’extension de nom de fichier personnalisée. si Lecteur Windows Media trouve un code de format, il utilise MTP pour déterminer si l’appareil prend en charge le format de fichier personnalisé. Si l’appareil prend en charge le format, le fichier multimédia est copié sur l’appareil sans être transcodé.

un appareil qui prend en charge MTP peut fournir Lecteur Windows Media avec un jeu de données DeviceInfo, qui contient, entre autres choses, une liste de codes de format pris en charge par l’appareil.

Si vous êtes en train de développer un format de fichier personnalisé, vous pouvez demander un code de format auprès de Microsoft. pour plus d’informations sur la demande d’un code de format, consultez le Kit de portage de protocole microsoft media Transport, disponible dans le [centre de développement microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’Extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




