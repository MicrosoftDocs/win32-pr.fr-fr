---
title: Raisons pour lesquelles les objets proxy sont nécessaires
description: Avec les objets accessibles, lorsqu’un client définit une fonction de raccordement dans le contexte, la DLL dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7038a43bf238d9baebee81e13cd82d904dc1b8a4c9ed7fb0c1576f42cbdfdfb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860989"
---
# <a name="why-proxy-objects-are-needed"></a>Raisons pour lesquelles les objets proxy sont nécessaires

Avec les objets accessibles, lorsqu’un client définit une [fonction de raccordement dans le contexte](in-context-and-out-of-context-hook-functions.md), la dll dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur. Dans ce cas, lorsque le client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) à partir de la fonction de raccordement, le pointeur d’interface qui est retourné pointe directement vers le code dans l’espace d’adressage du serveur. Lorsque le client appelle une propriété d’interface à l’aide de ce pointeur, la bibliothèque COM (Component Object Model) n’est pas impliquée dans le marshaling ou le démarshaling et ne peut pas détecter si un objet est détruit. Par conséquent, le serveur doit détecter cette situation et retourner un code d’erreur au client.

 

 




