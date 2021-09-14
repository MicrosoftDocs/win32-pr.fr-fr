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
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225540"
---
# <a name="xml-language-support"></a>Prise en charge du langage XML

Cette section décrit le niveau de prise en charge du langage XML dans WWS.


consultez les fonctions DownlevelLCIDToLocaleName sur les versions de Windows antérieures à Windows Vista, et LCIDToLocalName dans le cas contraire, pour effectuer une conversion entre un LCID et une valeur xml : lang.

Lors de la lecture, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) peut être utilisé pour découvrir la valeur d’un attribut « XML : lang » dans la portée.

Lors de l’écriture, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) peut être utilisé pour écrire un attribut "XML : lang".

 

 




