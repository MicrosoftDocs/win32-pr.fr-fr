---
description: Une fois qu’une image a été sélectionnée, une application utilise l’interface IWiaDataTransfer (pour les applications qui s’exécutent dans Windows XP ou une version antérieure) ou l’interface IWiaTransfer (pour les applications qui s’exécutent dans Windows Vista ou version ultérieure) pour transférer les données d’image des appareils d’images. Pour plus d’informations, consultez transfert de données d’image dans WIA 1,0 ou transfert de données d’image dans WIA 2,0.
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: Acquisition d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527489"
---
# <a name="acquiring-images"></a>Acquisition d’images

Une fois qu’une image a été sélectionnée, une application utilise l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (pour les applications qui s’exécutent dans Windows XP ou une version antérieure) ou l’interface [**IWiaTransfer**](-wia-iwiatransfer.md) (pour les applications qui s’exécutent dans Windows Vista ou version ultérieure) pour transférer les données d’image des appareils d’images. Pour plus d’informations, consultez [transfert de données d’image dans wia 1,0](-wia-transferring-image-data.md) ou [transfert de données d’image dans WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

Une fois qu’un appareil a été sélectionné, une application utilise la méthode [**IWiaItem ::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) de l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) de l’appareil (élément racine) pour sélectionner une image à partir d’un périphérique WIA (Windows Image Acquisition) spécifié. La méthode [**IWiaDevMgr :: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) affiche une boîte de dialogue qui permet à un utilisateur de sélectionner une image à partir d’un périphérique spécifié et de transférer l’image vers un nom de fichier sélectionné par l’utilisateur. Il permet également à l’utilisateur de spécifier un appareil, si nécessaire. Pour plus d’informations, consultez [sélection d’un appareil](-wia-selecting-a-device.md) .

Notez qu’il n’est pas nécessaire pour un utilisateur de sélectionner une image à l’aide de la méthode ci-dessus. Une application peut obtenir un pointeur vers un élément d’image directement à partir de l’arborescence d’éléments d’un appareil. Pour obtenir des instructions, consultez [navigation dans une arborescence d’éléments](-wia-navigating-an-item-tree.md).

Une fois que l’élément WIA qui représente l’image souhaitée a été sélectionné, une application s’exécutant sur Windows XP ou une version antérieure interroge l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) de cet élément pour obtenir un pointeur vers son interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) . Une application s’exécutant sur Windows Vista ou version ultérieure interroge l’interface [**IWiaItem2**](-wia-iwiaitem2.md) pour obtenir un pointeur vers son interface [**IWiaTransfer**](-wia-iwiatransfer.md) .

L’application peut ensuite utiliser les méthodes de l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (ou [**IWiaTransfer**](-wia-iwiatransfer.md)) pour transférer les données de l’image à l’application.

Si le périphérique d’acquisition d’images est un scanneur, [**IWiaDataTransfer :: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)ou d’autres méthodes de l’interface [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , déclenche une opération d’analyse, puis transfère les données d’image obtenues. Si l’appareil est un appareil photo, les données de l’image sont simplement transférées de l’appareil photo à l’application.

 

 



