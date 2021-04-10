---
title: Entrée de Registre FormatCode
description: Entrée de Registre FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Lecteur Windows Media, entrées de Registre FormatCode
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées FormatCode
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Entrées de Registre FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104198750"
---
# <a name="formatcode-registry-entry"></a>Entrée de Registre FormatCode

Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension. La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md). L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **FormatCode** .

L’entrée de Registre **FormatCode** spécifie le code de format MTP (Media Transport Protocol) pour les fichiers qui ont l’extension personnalisée. L’entrée de Registre **FormatCode** se présente sous la forme suivante.



| Nom       | Type           | Valeur                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **\_valeur DWORD reg** | Entier positif 16 bits qui identifie le format du fichier. |



 

Lorsque l’utilisateur tente de copier un fichier multimédia numérique ayant une extension de nom de fichier personnalisée sur un appareil mobile, le lecteur Windows Media recherche un code de format associé à l’extension de nom de fichier personnalisée dans le registre. Si le lecteur Windows Media trouve un code de format, il utilise MTP pour déterminer si l’appareil prend en charge le format de fichier personnalisé. Si l’appareil prend en charge le format, le fichier multimédia est copié sur l’appareil sans être transcodé.

Un appareil qui prend en charge MTP peut fournir le lecteur Windows Media avec un jeu de données DeviceInfo, qui contient, entre autres choses, une liste de codes de format pris en charge par l’appareil.

Si vous êtes en train de développer un format de fichier personnalisé, vous pouvez demander un code de format auprès de Microsoft. Pour plus d’informations sur la demande d’un code de format, consultez le kit de portage de protocole Microsoft Media transport, disponible dans le [Centre de développement Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




