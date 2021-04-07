---
title: Prise en charge des chaînes d’adresses IPX dans WinSNMP
description: WinSNMP 2,0 formalise l’utilisation des chaînes d’adresses IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671074"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Prise en charge des chaînes d’adresses IPX dans WinSNMP

WinSNMP 2,0 formalise l’utilisation des chaînes d’adresses IPX. Si vous spécifiez une chaîne d’adresse IPX comme paramètre d’entrée de la fonction [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , vous devez mettre en forme la chaîne en utilisant les normes suivantes :

-   Numéro de réseau composé de huit chiffres hexadécimaux (rempli à zéro si nécessaire)
-   Séparateur («  : », « . » ou « – »)
-   Numéro de nœud composé de 12 chiffres hexadécimaux (rempli à zéro si nécessaire)

Par exemple, 00000001:00081A0D01C2 ou 00000001.00081 a0d01c2. Les chiffres hexadécimaux peuvent être en majuscules ou en minuscules.

Il s’agit du format utilisé par la fonction [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) pour retourner une chaîne d’adresse IPX. La chaîne est retournée lorsqu’une application qui fonctionne dans l’un des modes SNMPAPI non \_ traduits appelle la fonction **SnmpEntityToStr** . La chaîne peut également être retournée lorsque l’application fonctionne en \_ mode de traduction SNMPAPI et qu’aucun nom convivial n’est disponible pour l’entité.

 

 




