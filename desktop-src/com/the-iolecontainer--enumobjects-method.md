---
title: Méthode IOleContainer EnumObjects
description: Méthode IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190841"
---
# <a name="the-iolecontainerenumobjects-method"></a>La méthode IOleContainer :: EnumObjects

Cette méthode est utilisée pour énumérer tous les objets OLE contenus dans un document ou un formulaire, en retournant un pointeur d’interface pour chaque objet OLE. Le conteneur doit renvoyer des pointeurs vers chaque objet OLE qui partage le même conteneur. Les formulaires imbriqués ou les contrôles imbriqués doivent également être énumérés.

Certains conteneurs implémentent des contrôles d’extendeur, qui encapsulent des contrôles non ActiveX, puis retournent des pointeurs vers ces contrôles d’extendeur au fur et à mesure qu’un formulaire est énuméré. Ce comportement permet aux contrôles ActiveX et aux conteneurs de contrôles ActiveX de s’intégrer parfaitement aux contrôles non ActiveX. il est donc recommandé, mais pas obligatoire.

 

 




