---
title: Longueur de la mémoire tampon des fonctions de gestion de réseau
description: Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194708"
---
# <a name="network-management-function-buffer-lengths"></a>Longueur de la mémoire tampon des fonctions de gestion de réseau

Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.

Les applications qui spécifient des tailles de mémoire tampon lors de l’appel de fonctions d’énumération de gestion de réseau (et diverses fonctions de récupération de données) doivent spécifier des mémoires tampons suffisamment grandes pour contenir la structure d’informations (ou structures) retournées, ainsi que les chaînes auxquelles leurs membres pointent. Si vous ne spécifiez pas de mémoire tampon suffisamment grande pour recevoir toutes les entrées disponibles, la fonction retourne l’erreur \_ plus de \_ données. Les appels d’énumération ne retournent pas d’entrées partielles.

Certaines fonctions de gestion de réseau prennent un paramètre de longueur de données maximal de l’avis, *prefmaxlen*. Ce paramètre permet à une application de suggérer le nombre d’octets que le serveur doit retourner à partir d’un appel de fonction.

Si vous spécifiez la valeur MAX \_ préférée \_ Length dans le paramètre *prefmaxlen* , les fonctions de gestion de réseau allouent la quantité de mémoire requise pour les données.

Pour plus d’informations, consultez [mémoires tampons de fonctions de gestion de réseau](network-management-function-buffers.md).

 

 




