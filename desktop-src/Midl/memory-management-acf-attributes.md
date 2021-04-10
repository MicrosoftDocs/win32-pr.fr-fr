---
title: Attributs ACF de gestion de la mémoire
description: Les attributs figurant dans le tableau suivant vous permettent d’effectuer la gestion de la mémoire du côté client.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL, attributs, gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940936"
---
# <a name="memory-management-acf-attributes"></a>Attributs ACF de gestion de la mémoire

Les attributs figurant dans le tableau suivant vous permettent d’effectuer la gestion de la mémoire du côté client.



| Attribut                                   | Utilisation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lui**](allocate.md)                | Spécifie la façon dont l’application cliente et le stub allouent et libèrent de la mémoire pour les pointeurs. Cet attribut est particulièrement utile lorsque vous souhaitez que certaines structures de pointeur restent accessibles à l’application serveur après que l’appel de procédure distante a été retourné au client. Vous pouvez également utiliser l’attribut [**allocate**](allocate.md) pour indiquer au stub de calculer la taille de la mémoire référencée par le pointeur du type spécifié et d’effectuer un appel unique à [**l' \_ \_ allocation d’utilisateur MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**nombre d’octets \_**](byte-count.md)           | Vous permet de créer un bloc de mémoire persistant et contigu qui peut être réutilisé sur plusieurs appels de procédure distante. Cela libère l’application cliente de la surcharge d’allocation et de libération de mémoire qui peut inclure plusieurs pointeurs et d’autres structures de données complexes.                                                                                                                                                                                                                                                      |
| [**activer l' \_ allocation**](enable-allocate.md) | Spécifie que le code stub du serveur doit activer l’environnement de gestion de mémoire stub.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 