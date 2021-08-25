---
title: Chaînes incorporées
description: Les structures d’informations ne contiennent pas de chaînes incorporées. Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6121e805a1dbe329cee52a760c809ded21f1740b19adaa3e18eaa5033fd15897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912249"
---
# <a name="embedded-strings"></a>Chaînes incorporées

Les structures d’informations ne contiennent pas de chaînes incorporées. Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.

Tout champ d’information retourné dans un appel d’énumération qui peut être utilisé par la suite comme clé pour l’appel à une fonction de gestion réseau GetInfo est toujours présent dans la mémoire tampon d’énumération. Si la chaîne d’informations de longueur variable qui spécifie la valeur du champ clé ne peut pas être contenue, l’intégralité de la structure de longueur fixe de l’entrée n’est pas retournée. D’autres champs de longueur variable sont retournés en tant que pointeur **null** pour le cas dans lequel la chaîne ne tient pas.

 

 




