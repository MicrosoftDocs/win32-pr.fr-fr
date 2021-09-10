---
title: Recherche d’un pilote spécifique
description: Recherche d’un pilote spécifique
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Gestionnaire de compression audio (ACM), recherche de pilotes
- ACM (gestionnaire de compression audio), recherche de pilotes
- Exemples ACM, recherche de pilotes
- recherche de pilotes
- acmDriverEnum fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364060"
---
# <a name="finding-a-specific-driver"></a>Recherche d’un pilote spécifique

Vous pouvez souhaiter que votre application envoie un message directement à un pilote spécifique ou pour identifier certains pilotes de la liste. Par exemple, vous souhaiterez peut-être que votre application identifie les pilotes qui prennent en charge les filtres, puis interroger chaque pilote pour déterminer les balises de filtre qu’il prend en charge. Vous pouvez utiliser la fonction [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) pour obtenir un handle pour le ou les pilotes souhaités. ce descripteur peut ensuite être utilisé pour communiquer avec ce pilote.

Notez que lorsqu’une application installe un pilote local pour son propre usage, la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) retourne un handle de pilote, qui peut être utilisé pour communiquer avec le pilote. Dans ce cas, il n’est pas nécessaire d’utiliser **acmDriverEnum** .

 

 




