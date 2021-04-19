---
description: Outre l’activation de la surveillance des chiffres et la notification d’un chiffre à la fois, une application peut également demander que plusieurs chiffres soient collectés dans une mémoire tampon.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Collecte des chiffres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519614"
---
# <a name="digit-gathering"></a>Collecte des chiffres

Outre l’activation de la surveillance des chiffres et la notification d’un chiffre à la fois, une application peut également demander que plusieurs chiffres soient collectés dans une mémoire tampon. L’application est notifiée uniquement lorsque la mémoire tampon est saturée ou qu’une autre condition d’arrêt est remplie. La collecte des chiffres est utile pour les fonctions telles que la collecte des numéros de carte de crédit. Elle est exécutée lorsqu’une application appelle [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), en spécifiant une mémoire tampon à remplir avec des chiffres. La collecte des chiffres se termine lorsque l’une des conditions suivantes est remplie :

-   Le nombre de chiffres demandé a été collecté.
-   Un ou plusieurs caractères de fin sont détectés. Les chiffres de fin sont spécifiés à [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)et le chiffre d’arrêt est également placé dans la mémoire tampon.
-   L’un des deux délais d’attente expire. Les délais d’expiration sont un délai d’expiration pour le premier chiffre, qui spécifie la durée maximale avant que le premier chiffre soit collecté et un délai d’expiration inter-chiffres, spécifiant la durée maximale entre les chiffres successifs.
-   La collecte de chiffres est de nouveau annulée explicitement par [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) avec un autre ensemble de paramètres pour démarrer une nouvelle demande de collecte ou en utilisant un paramètre de mémoire tampon de chiffres **null** pour annuler.

Lorsque la collecte des chiffres se termine pour une raison quelconque, un message [**\_ GATHERDIGITS de ligne**](line-gatherdigits.md) est envoyé à l’application qui a demandé la collecte des chiffres. Une seule demande de collecte de chiffres peut être en suspens sur un appel à un moment donné dans toutes les applications qui sont propriétaires de l’appel.

La collecte des chiffres et la surveillance des chiffres peuvent être activées simultanément sur un même appel. Dans ce cas, l’application reçoit un message de [**ligne \_ MONITORDIGITS**](line-monitordigits.md) pour chaque chiffre détecté et un message de GATHERDIGITS de ligne distinct \_ lorsque la mémoire tampon est renvoyée.

 

 



