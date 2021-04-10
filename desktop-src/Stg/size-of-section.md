---
title: Taille de la section
description: Le type de données de la taille de la section indique la taille, en octets, de la section.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197343"
---
# <a name="size-of-section"></a>Taille de la section

Le type de données de la taille de la section indique la taille, en octets, de la section. Étant donné que la taille de la section est les 4 premiers octets, les sections peuvent être copiées sous la forme d’un tableau d’octets. La taille de la section doit toujours être un multiple de quatre.

Par exemple, une section vide, autrement dit, l’une avec les propriétés zéro, aurait un nombre d’octets de huit (le nombre d’octets **DWORD** et le nombre de propriétés **DWORD** ). La section elle-même contient les 8 octets suivants : **08 00 00 00 00 00 00 00**.

 

 




