---
description: Les applications voient les périphériques WIA (Windows Image Acquisition) comme une arborescence hiérarchique d’objets IWiaItem ou IWiaItem2 avec l’élément racine représentant l’appareil lui-même.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: Minipilote WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526410"
---
# <a name="wia-minidriver"></a>Minipilote WIA

Les applications voient les périphériques WIA (Windows Image Acquisition) comme une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) avec l’élément racine représentant l’appareil lui-même. Les appareils WIA peuvent être utilisés simultanément par plusieurs applications. C’est pourquoi il est nécessaire que l’affichage de chaque application d’un objet **IWiaItem** ou **IWiaItem2** soit indépendant des vues d’une autre application. Pour ce faire, vous devez disposer de deux objets Item différents. Le pilote crée l’arborescence d’éléments de pilote des objets d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , également appelés éléments de pilote, à l’aide des méthodes de services de pilote WIA. Il s’agit d’objets globaux que le pilote utilise pour représenter les éléments internes de chaque pilote. Quand une application crée un objet **IWiaItem** ou **IWiaItem2** (également appelé élément d’application), cet objet est lié à l' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondante du pilote dans l’arborescence d’éléments du pilote. Un décompte de références est conservé sur l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) en fonction des règles suivantes :

-   Lorsqu’un pilote ajoute un objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) à l’arborescence des éléments du pilote, le nombre de références de l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est incrémenté. Cela se produit généralement lors du traitement de [IWiaMiniDrv ::D rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) ou lorsqu’une \_ commande WIA cmd \_ Synchronize est traitée.
-   Lorsqu’un pilote supprime un objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) de l’arborescence d’éléments de pilote, le décompte de références de l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est décrémenté et l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est marqué afin qu’il ne puisse plus accéder à l’appareil. Cela se produit généralement lorsqu’un appareil est déconnecté ou qu’un élément est supprimé. Les applications sont toujours en mesure de lire des propriétés à partir d’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) , même lorsque l’objet [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondant a été supprimé de l’arborescence des éléments du pilote.
-   Lorsqu’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) est créé, il est lié à un objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondant. Le décompte de références de l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est incrémenté.
-   Lorsqu’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) est libéré, le lien vers l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondant est interrompu et le décompte de références de l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est décrémenté.
-   Si le décompte de références d’un objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) atteint zéro, l’objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) est supprimé. Cela s’applique à tous les objets d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , y compris l’élément racine. Le décompte de références d’un objet d' [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) passe à zéro uniquement lorsqu’aucun élément d’application ne le référence et qu’il n’est plus lié à l’arborescence d’éléments du pilote.

À l’aide de ce schéma de décompte de références, de nombreux objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) peuvent être liés à une [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sans interférence. Étant donné que chaque **IWiaItem** ou **IWiaItem2** contient son propre stockage de propriétés, une application peut continuer à lire les propriétés de l’élément, même après la suppression d’un élément, mais aucune opération nécessitant l’accès à l’appareil ne sera effectuée. Étant donné que les propriétés de l’élément sont stockées dans l’objet **IWiaItem** ou **IWiaItem2** , le pilote doit définir les propriétés de l’objet **IWiaItem** ou **IWiaItem2** sur l’appareil avant un transfert de données.

 

 



