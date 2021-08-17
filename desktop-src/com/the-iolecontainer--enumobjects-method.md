---
title: Méthode IOleContainer EnumObjects
description: Méthode IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd74e4916eec4d58240f702a09fd8376008fe0bb352113e1512bd2882d8dee9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462319"
---
# <a name="the-iolecontainerenumobjects-method"></a>La méthode IOleContainer :: EnumObjects

Cette méthode est utilisée pour énumérer tous les objets OLE contenus dans un document ou un formulaire, en retournant un pointeur d’interface pour chaque objet OLE. Le conteneur doit renvoyer des pointeurs vers chaque objet OLE qui partage le même conteneur. Les formulaires imbriqués ou les contrôles imbriqués doivent également être énumérés.

certains conteneurs implémentent des contrôles d’extendeur, qui encapsulent des contrôles non ActiveX, puis retournent des pointeurs vers ces contrôles d’extendeur lorsqu’un formulaire est énuméré. ce comportement permet aux contrôles de ActiveX et aux conteneurs de contrôle ActiveX de s’intégrer parfaitement aux contrôles non ActiveX et est donc recommandé, mais pas obligatoire.

 

 




