---
title: Raisons pour lesquelles les objets proxy sont nécessaires
description: Avec les objets accessibles, lorsqu’un client définit une fonction de raccordement dans le contexte, la DLL dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309998"
---
# <a name="why-proxy-objects-are-needed"></a>Raisons pour lesquelles les objets proxy sont nécessaires

Avec les objets accessibles, lorsqu’un client définit une [fonction de raccordement dans le contexte](in-context-and-out-of-context-hook-functions.md), la dll dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur. Dans ce cas, lorsque le client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) à partir de la fonction de raccordement, le pointeur d’interface qui est retourné pointe directement vers le code dans l’espace d’adressage du serveur. Lorsque le client appelle une propriété d’interface à l’aide de ce pointeur, la bibliothèque COM (Component Object Model) n’est pas impliquée dans le marshaling ou le démarshaling et ne peut pas détecter si un objet est détruit. Par conséquent, le serveur doit détecter cette situation et retourner un code d’erreur au client.

 

 




