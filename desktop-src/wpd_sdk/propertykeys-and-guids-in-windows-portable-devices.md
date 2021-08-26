---
description: PROPERTYKEYs et guid dans Windows appareils mobiles
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs et guid dans Windows appareils mobiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80100b043383074f58bc27fe8e9782c4fd6d2e4f3841a28f37035f39d23cc7c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054869"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>PROPERTYKEYs et guid dans Windows appareils mobiles

Une propriété ou une commande est identifiée par une structure PROPERTYKEY. Une structure PROPERTYKEY est constituée de deux parties : un GUID (le membre fmtid) et un DWORD (le membre PID). La partie GUID est utilisée pour indiquer la catégorie à laquelle appartient la propriété ou la commande (autrement dit, les propriétés associées appartiennent à la même catégorie et les commandes associées appartiennent à la même catégorie ; elles ont donc le même fmtid). La partie DWORD indique la propriété ou l’ID de commande et est utilisée pour distinguer les propriétés ou les commandes individuelles au sein d’une catégorie de propriété ou de commande (autrement dit, les valeurs PID pour les propriétés ou les commandes dans la même catégorie seront différentes).

La section Références de ce document décrit toutes les valeurs de PROPERTYKEY définies par WPD. ces valeurs correspondent à des commandes, des propriétés et des ressources. Si vous créez une valeur PROPERTYKEY personnalisée, vous devez définir une nouvelle catégorie **GUID** ; ne réutilisez pas les valeurs de **GUID** wpd ou risquez d’être en conflit avec les valeurs PROPERTYKEYs existantes et futures spécifiées dans wpd.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> <dt>

[**Commandes**](commands.md)
</dt> <dt>

[**GUID de format d’objet**](object-format-guids.md)
</dt> <dt>

[**Propriétés et attributs**](properties-and-attributes.md)
</dt> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 



