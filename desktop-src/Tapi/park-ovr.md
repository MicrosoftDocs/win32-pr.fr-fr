---
description: L’opération de parc permet à une application d’envoyer une session à une adresse spéciale à laquelle elle sera conservée jusqu’à ce qu’elle soit désimmobilisée.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Parcs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518710"
---
# <a name="park"></a>Parcs

L’opération de parc permet à une application d’envoyer une session à une adresse spéciale à laquelle elle sera conservée jusqu’à ce qu’elle soit désimmobilisée. Du point de vue de l’application, cela ressemble à un transfert. Pour le tiers situé à l’autre extrémité de la connexion, cela ressemble à la mise en attente.

La différence entre le stationnement et le transfert réside dans le fait que l’adresse en stationnement n’est pas un point de connexion pour la session et que la session n’est pas avertie ou expire. La différence entre le stationnement et le blocage est qu’une fois l’opération de parc terminée, la session n’est plus associée à l’adresse de l’application.

Deux formes de parking une session sont fournies : le stationnement *dirigé* et le parking *indirect*. Dans le parc d’appels dirigés, l’application spécifie l’adresse de destination dans laquelle l’appel doit être parqué. Avec un parking indirect, le fournisseur de services ou le matériel sous-jacent détermine l’adresse et la renvoie à l’application.

Une session parqué passe généralement en état d’inactivité une fois qu’elle a été correctement importée, et l’application doit ensuite libérer les ressources qui lui sont associées. Pour obtenir un résumé de la procédure à suivre, consultez [terminer une session](terminate-a-session-ovr.md) .

Si l’application désintègre la session, de nouvelles ressources de session sont allouées même si l’application a renvoyé les pointeurs précédents, si bien que l’échec des mises en production correctes peut entraîner de nombreux problèmes.

Certains fournisseurs de services peuvent rappeler à l’utilisateur une fois qu’une session a été immobilisée pendant un certain laps de temps. L’application voit un appel d’offre avec une [raison](reason-ovr.md) d’appel définie sur rappel.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3 :** Consultez [**ITBasicCallControl ::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl ::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl :: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
