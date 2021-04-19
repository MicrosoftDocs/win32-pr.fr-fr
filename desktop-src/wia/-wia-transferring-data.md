---
description: 'En savoir plus sur : transfert de données'
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: Transfert de données
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536971"
---
# <a name="transferring-data"></a><span data-ttu-id="c60c1-103">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="c60c1-103">Transferring Data</span></span>

> [!Note]  
> <span data-ttu-id="c60c1-104">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="c60c1-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="c60c1-105">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="c60c1-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="c60c1-106">Utilisez la méthode de [**transfert**](-wia-iwiadispatchitem-transfer.md) d’un objet [**Item**](-wia-item.md) pour transférer des données d’image ou audio d’un appareil vers un fichier ou le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="c60c1-106">Use the [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of an [**Item**](-wia-item.md) object to transfer image or audio data from a device to a file or the clipboard.</span></span>

<span data-ttu-id="c60c1-107">Transmettez un chemin d’accès et un nom de fichier en tant que premier paramètre pour enregistrer les données sur le disque, ou transmettez la chaîne « Clipboard » pour transférer l’élément dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="c60c1-107">Pass a path and filename as the first parameter to save the data to disk, or pass the string "clipboard" to transfer the item to the clipboard.</span></span>

 

 
