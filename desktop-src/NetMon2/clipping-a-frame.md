---
description: Vous pouvez spécifier que le pilote découpe les frames.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Découpage d’un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9251fc6f8a1c9612a9fa7301ea8948956291ad0d074f90ff2ccbbf3f799bd2b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911259"
---
# <a name="clipping-a-frame"></a>Découpage d’un frame

Vous pouvez spécifier que le pilote découpe les frames. (Si les autres sections de filtre de capture sont omises, il peut s’agir de la seule fonction de votre filtre de capture). Si le champ **nFrameBytesToCopy** n’est pas égal à zéro (0), sa valeur spécifie le nombre d’octets de chaque trame reçus à conserver. Si le champ est égal à zéro, le frame entier est conservé.

> [!Note]  
> Vous pouvez découper n’importe quel frame qui transmet les autres parties de votre filtre de capture en définissant **nFrameBytesToCopy**.

 

 

 



