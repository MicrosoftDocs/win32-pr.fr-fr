---
title: Handles de reprise d’énumération
description: Les handles de reprise d’énumération sont des identificateurs pour la clé de reprise réelle contenue dans les données d’instance de la fonction. Cela est nécessaire pour la sécurité, l’interopérabilité et pour simplifier le code de l’appelant pour la fonction.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10976661723af59af945b9dec1080196e682b308fa1a597edfc4cee6047aa783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912189"
---
# <a name="enumeration-resume-handles"></a>Handles de reprise d’énumération

Les handles de reprise d’énumération sont des identificateurs pour la clé de reprise réelle contenue dans les données d’instance de la fonction. Cela est nécessaire pour la sécurité, l’interopérabilité et pour simplifier le code de l’appelant pour la fonction.

Si une **valeur null** est transmise pour le pointeur vers le handle de reprise, aucun handle n’est stocké et la recherche d’énumération ne peut pas être poursuivie. Cela est utile dans les cas où l’application ne souhaite pas énumérer tous les éléments.

Si une erreur est retournée à partir d’un appel d’énumération, le handle de reprise doit être traité comme non valide et n’est pas utilisé pour les appels d’énumération suivants. Lorsque cela se produit, vous devez redémarrer l’énumération depuis le début.

 

 




