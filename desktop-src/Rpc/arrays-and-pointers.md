---
title: Tableaux et pointeurs
description: L’appel de procédure distante (RPC) est conçu pour être principalement transparent pour les développeurs.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Appel de procédure distante RPC, décrit, tableaux et pointeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073499"
---
# <a name="arrays-and-pointers"></a>Tableaux et pointeurs

L’appel de procédure distante (RPC) est conçu pour être principalement transparent pour les développeurs. Pour atteindre cette transparence, le stub client transmet au serveur le pointeur et l’objet de données vers lequel il pointe. Si la procédure distante modifie les données, le serveur doit transmettre les nouvelles données au client afin que le client puisse copier les nouvelles données sur les données d’origine.

En général, un appel de procédure distante se comporte comme un appel de procédure local. Autrement dit, lorsqu’un pointeur est un paramètre, la procédure distante peut accéder à l’objet de données auquel le pointeur fait référence de la même façon qu’une procédure locale.

Étant donné que les programmes client et serveur s’exécutent dans différents espaces d’adressage, les développeurs doivent utiliser des attributs Microsoft Interface Definition Language (MIDL) pour décrire la façon dont les données de tableau et de pointeur sont transmises entre le client et le serveur. Cette section présente une vue d’ensemble de l’utilisation des tableaux et des pointeurs dans les applications distribuées, dans les rubriques suivantes :

-   [Tableaux et RPC](arrays-and-rpc.md)
-   [Pointeurs et RPC](pointers-and-rpc.md)
-   [Utilisation de tableaux, de chaînes et de pointeurs](using-arrays-strings-and-pointers.md)

 

 




