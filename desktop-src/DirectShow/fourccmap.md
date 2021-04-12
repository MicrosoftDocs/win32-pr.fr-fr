---
description: La classe FOURCCMap fournit la conversion entre les sous-types de média GUID et les balises multimédias FOURCC 32 bits de style ancien.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109202"
---
# <a name="fourccmap-class"></a>FOURCCMap, classe

![hiérarchie de la classe fourccmap](images/fourcc01.png)

La classe **FOURCCMap** fournit la conversion entre les sous-types de média **GUID** et les balises multimédias **FourCC** 32 bits de style ancien. Dans les API multimédia Windows d’origine, les types de média ont été marqués avec des valeurs 32 bits créées à partir de caractères 4 8 bits et connues sous le nom de « **FourCC** s ». Les types de média DirectShow ont des **GUID** pour le sous-type, en partie parce qu’ils sont plus simples à créer (la création d’un nouveau **FourCC** nécessite son inscription auprès de Microsoft). Étant donné que les valeurs **FourCC** sont uniques, un mappage un-à-un est rendu possible en allouant une plage de 4 milliards **GUID** représentant des **FourCC** s. Cette plage correspond à tous les **GUID** sous la forme :

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Cette classe simplifie la conversion entre les **GUID** s et **FourCC**. Il s’agit d’une compatibilité uniquement. Il est recommandé que tous les nouveaux sous-types de médias soient représentés par les **GUID** créés par Guidgen.exe ou un outil similaire, et non par le mappage de **FourCC** s.

L’objet est dérivé d’un **GUID**, sans données membres supplémentaires, et peut faire l’objet d’un cast en **GUID**. Un **FourCC** peut être passé à l’objet au moment de la construction. Le constructeur par défaut initialise le **FourCC** à zéro.

Les méthodes [**GetFOURCC**](fourccmap-getfourcc.md) et [**SetFOURCC**](fourccmap-setfourcc.md) ne vérifient pas que les parties fixes du **GUID** correspondent à la plage **FourCC** . Ainsi, si vous effectuez un cast d’un pointeur vers un **GUID** en un pointeur vers un **FourCC** , puis que vous définissez ou récupérez le champ **FourCC** , vous devez également vérifier séparément que le **GUID** se trouve dans la plage **FourCC** .

## <a name="member-functions"></a>Fonctions de membre



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Méthode de constructeur.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Récupère le **FourCC** à partir d’un objet **FOURCCMap** .    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Définit la partie **FourCC** de l’objet **FOURCCMap** . |



 

 

 



