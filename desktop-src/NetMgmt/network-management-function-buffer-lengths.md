---
title: Longueur de la mémoire tampon des fonctions de gestion de réseau
description: Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858b01de7b0b4cecb9eaea9f93bb541cb95fe9b394e74616427910abe3b33403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911739"
---
# <a name="network-management-function-buffer-lengths"></a>Longueur de la mémoire tampon des fonctions de gestion de réseau

Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.

Les applications qui spécifient des tailles de mémoire tampon lors de l’appel de fonctions d’énumération de gestion de réseau (et diverses fonctions de récupération de données) doivent spécifier des mémoires tampons suffisamment grandes pour contenir la structure d’informations (ou structures) retournées, ainsi que les chaînes auxquelles leurs membres pointent. Si vous ne spécifiez pas de mémoire tampon suffisamment grande pour recevoir toutes les entrées disponibles, la fonction retourne l’erreur \_ plus de \_ données. Les appels d’énumération ne retournent pas d’entrées partielles.

Certaines fonctions de gestion de réseau prennent un paramètre de longueur de données maximal de l’avis, *prefmaxlen*. Ce paramètre permet à une application de suggérer le nombre d’octets que le serveur doit retourner à partir d’un appel de fonction.

Si vous spécifiez la valeur MAX \_ préférée \_ Length dans le paramètre *prefmaxlen* , les fonctions de gestion de réseau allouent la quantité de mémoire requise pour les données.

Pour plus d’informations, consultez [mémoires tampons de fonctions de gestion de réseau](network-management-function-buffers.md).

 

 




