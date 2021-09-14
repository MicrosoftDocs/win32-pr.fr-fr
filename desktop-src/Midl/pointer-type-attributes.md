---
title: Attributs de type pointeur
description: Les attributs suivants spécifient les caractéristiques des pointeurs.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL, attributs, pointer-type
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093265"
---
# <a name="pointer-type-attributes"></a>Attributs de type pointeur

Les attributs suivants spécifient les caractéristiques des pointeurs.



| Attribut                                   | Usage                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Désigne un pointeur comme pointeur complet, avec toutes les fonctionnalités d’un pointeur en langage C, y compris les alias.                                                                                       |
| [**ref**](ref.md)                          | Désigne le type de pointeur le plus simple dans MIDL, un qui fournit simplement l’adresse de certaines données. Les pointeurs de référence ne peuvent jamais avoir la valeur null.                                                             |
| [**unique**](unique.md)                    | Permet à un pointeur d’avoir la valeur null, mais ne prend pas en charge les alias.                                                                                                                                               |
| [**pointeur \_ par défaut**](pointer-default.md) | Appliqué à une interface pour spécifier le type de pointeur par défaut pour tous les pointeurs de cette interface, à l’exception des pointeurs de paramètre de niveau supérieur, qui sont automatiquement par défaut des pointeurs [**ref**](ref.md) . |
| [**IID \_ est**](iid-is.md)                   | Fournit l’identificateur d’interface de l’interface COM qui est l’objet du pointeur.                                                                                                            |
| [**chaîne**](string.md)                    | Spécifie que le pointeur pointe vers une chaîne.                                                                                                                                                       |



 

 

 




