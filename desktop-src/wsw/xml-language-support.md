---
title: Prise en charge du langage XML
description: Cette section décrit le niveau de prise en charge du langage XML dans WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Services Web de prise en charge du langage XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebcf9eae98e15778fb95b47db2253bf553da16336317f7cdee69c20aa298584c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880719"
---
# <a name="xml-language-support"></a>Prise en charge du langage XML

Cette section décrit le niveau de prise en charge du langage XML dans WWS.


consultez les fonctions DownlevelLCIDToLocaleName sur les versions de Windows antérieures à Windows Vista, et LCIDToLocalName dans le cas contraire, pour effectuer une conversion entre un LCID et une valeur xml : lang.

Lors de la lecture, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) peut être utilisé pour découvrir la valeur d’un attribut « XML : lang » dans la portée.

Lors de l’écriture, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) peut être utilisé pour écrire un attribut "XML : lang".

 

 




