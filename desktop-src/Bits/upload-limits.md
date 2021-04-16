---
title: Limites de téléchargement
description: Pour limiter la taille des chargements, définissez la propriété d’extension IIS BITSMaximumUploadSize.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462719"
---
# <a name="upload-limits"></a>Limites de téléchargement

Pour limiter la taille des chargements, définissez la propriété d’extension IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) . Dans IIS 7, vous devrez peut-être également modifier l’attribut **maxAllowedContentLength** . Par défaut, la limite de téléchargement d’IIS 7 est de 30 millions octets. Pour plus d’informations sur la modification de la valeur par défaut IIS, consultez [KB942074](https://support.microsoft.com//kb/942074).

 

 




