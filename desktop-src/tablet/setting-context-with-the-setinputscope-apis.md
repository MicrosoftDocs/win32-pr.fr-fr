---
description: La technique de programmation recommandée pour définir des contextes dans une application qui n’est pas compatible avec l’encre consiste à utiliser les fonctions SetInputScope pour associer le contexte aux champs de l’application.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Définition du contexte avec les API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544933"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Définition du contexte avec les API SetInputScope

La technique de programmation recommandée pour définir des contextes dans une application qui n’est pas compatible avec l’encre consiste à utiliser les fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) pour associer le contexte aux champs de l’application.

Le kit de développement Microsoft Windows XP Tablet PC Edition 1,7 était la première version de Microsoft Windows à offrir [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows Vista prend également en charge ces fonctions. Les définitions **SetInputScope** sont déclarées dans InputScope. idl et InputScope. h. Pour plus d’informations, consultez [Text Services Framework](../tsf/text-services-framework.md).

Les fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sont la méthode recommandée pour définir le contexte pour les contrôles et les applications qui ne sont pas activés par l’encre.

## <a name="common-input-scopes"></a>Étendues d’entrée courantes

À l’aide des fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) et du jeu défini d’étendues d’entrée communes décrites dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , vous pouvez améliorer la précision de la reconnaissance des reconnaissance de l’écriture manuscrite Microsoft.

> [!Note]  
> Les programmes de reconnaissance pour l’anglais (États-Unis), l’anglais (Royaume-Uni), l’allemand, le français, l’italien, l’espagnol, le néerlandais et le portugais prennent actuellement en charge l’utilisation des étendues d’entrée courantes avec [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
