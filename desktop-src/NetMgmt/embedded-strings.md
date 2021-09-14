---
title: Chaînes incorporées
description: Les structures d’informations ne contiennent pas de chaînes incorporées. Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009417"
---
# <a name="embedded-strings"></a>Chaînes incorporées

Les structures d’informations ne contiennent pas de chaînes incorporées. Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.

Tout champ d’information retourné dans un appel d’énumération qui peut être utilisé par la suite comme clé pour l’appel à une fonction de gestion réseau GetInfo est toujours présent dans la mémoire tampon d’énumération. Si la chaîne d’informations de longueur variable qui spécifie la valeur du champ clé ne peut pas être contenue, l’intégralité de la structure de longueur fixe de l’entrée n’est pas retournée. D’autres champs de longueur variable sont retournés en tant que pointeur **null** pour le cas dans lequel la chaîne ne tient pas.

 

 




