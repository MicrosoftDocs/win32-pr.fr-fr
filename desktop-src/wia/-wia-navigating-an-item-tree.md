---
description: Une application parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil. À l’aide de cette technique, une application sélectionne et acquiert une image sans présenter une boîte de dialogue à l’utilisateur.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navigation dans une arborescence d’éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526433"
---
# <a name="navigating-an-item-tree"></a>Navigation dans une arborescence d’éléments

Une application parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil. À l’aide de cette technique, une application sélectionne et acquiert une image sans présenter une boîte de dialogue à l’utilisateur.

Un appareil WIA est représenté en tant qu’élément racine dans une arborescence d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) . Les éléments enfants de l’arborescence représentent les images d’un scanneur ou d’un appareil photo.

Une fois qu’un appareil WIA est sélectionné, une application appelle la méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) de l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) de l’appareil pour énumérer les éléments enfants (les images ou les lits d’analyse) de l’appareil. Pour obtenir des instructions, consultez [sélection d’un appareil](-wia-selecting-a-device.md).

La méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crée un objet d’énumération pour les éléments enfants de l’appareil et retourne un pointeur vers l’interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) de cet objet. L’application peut ensuite utiliser les méthodes de l’interface **IEnumWiaItem** pour obtenir des pointeurs vers les éléments de l’arborescence d’éléments de l’appareil.

 

 



