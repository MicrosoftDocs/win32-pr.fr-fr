---
description: L’API WiFi Native contient des fonctions, des structures et des énumérations qui prennent en charge la connectivité de réseau sans fil et la gestion des profils sans fil.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: À propos de l’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fafbe65d162668930470712c79637a41fcd0ee0769441b745e68bca156ada4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685459"
---
# <a name="about-the-native-wifi-api"></a>À propos de l’API WiFi Native

L’API WiFi Native contient des fonctions, des structures et des énumérations qui prennent en charge la connectivité de réseau sans fil et la gestion des profils sans fil. L’API peut être utilisée pour les réseaux d’infrastructure et ad hoc. L’API ad hoc sans fil est une interface simplifiée orientée objet pour la création, la gestion et l’utilisation de réseaux ad hoc.

> [!Note]  
> Le mode ad hoc n’est peut-être pas disponible dans les versions ultérieures de Windows. à partir de Windows 8.1 et Windows Server 2012 R2, utilisez [Wi-Fi Direct](about-the-wi-fi-direct-api.md) à la place.

 

L’implémentation de l’API ad hoc utilise l’API WiFi native. Cela signifie que les appels d’API ad hoc peuvent déclencher des notifications WiFi natives, et vice versa.

Il n’est pas recommandé de combiner les appels d’API WiFi natives et les appels d’API ad hoc sans fil. Les développeurs doivent choisir une approche de programmation avant de concevoir une application. Si votre application utilise ou gère des réseaux d’infrastructure, vous devez utiliser l’API WiFi native. Si votre application nécessite une fonctionnalité de gestion des profils, vous devez utiliser l’API WiFi native. Dans le cas contraire, vous devez utiliser l’API ad hoc sans fil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la WiFi Native](about-native-wifi.md)
</dt> <dt>

[prise en charge de l’API Wifi Native sur Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[Autorisations de l’API WiFi Native](native-wifi-api-permissions.md)
</dt> <dt>

[À propos de l’API ad hoc sans fil](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[télécharger le kit de développement logiciel (SDK) Windows Vista](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



