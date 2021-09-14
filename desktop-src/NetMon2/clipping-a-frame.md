---
description: Vous pouvez spécifier que le pilote découpe les frames.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Découpage d’un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222753"
---
# <a name="clipping-a-frame"></a>Découpage d’un frame

Vous pouvez spécifier que le pilote découpe les frames. (Si les autres sections de filtre de capture sont omises, il peut s’agir de la seule fonction de votre filtre de capture). Si le champ **nFrameBytesToCopy** n’est pas égal à zéro (0), sa valeur spécifie le nombre d’octets de chaque trame reçus à conserver. Si le champ est égal à zéro, le frame entier est conservé.

> [!Note]  
> Vous pouvez découper n’importe quel frame qui transmet les autres parties de votre filtre de capture en définissant **nFrameBytesToCopy**.

 

 

 



