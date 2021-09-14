---
description: Les applications TAPI résident dans leur propre espace de processus.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Vue d’ensemble du fournisseur de services TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416308"
---
# <a name="tapi-service-provider-overview"></a>Vue d’ensemble du fournisseur de services TAPI

Les applications TAPI résident dans leur propre espace de processus. Les applications TAPI chargent les Tapi32.dll ou Tapi3.dll dans leur processus, et l’interface TAPI communique avec TAPISRV via une interface RPC privée. Un TSP s’exécute dans le contexte de TAPISRV. Un TSP donné peut résider sur un ordinateur autre que l’ordinateur de l’utilisateur et est accessible à l’aide d’un TSP distant. TAPISRV est implémenté en tant que processus de service dans SVCHOST. Un MSP réside dans l’espace de processus de l’application et est toujours local.

Une paire TSP/MSP peut être considérée comme ayant un chemin de communication privé virtuel. Les informations peuvent être envoyées entre les deux à l’aide de mémoires tampon opaques qui ne sont pas interprétées par TAPISRV ou par la DLL TAPI.

Certains fournisseurs de services implémentent des opérations spécifiques au matériel impliqué. TAPI 2. x donne accès à ces opérations via la fonction [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) ou [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . TAPI 3. x expose [des interfaces spécifiques au fournisseur](./provider-specific-interfaces.md).

Le diagramme suivant illustre le déroulement des contrôles et des informations, en montrant un TSP autonome (Unimodem) et une paire TSP/MSP (H. 323).

![PVC autonome et le flot de contrôle et d’informations du PVC/MSP couplé](images/tsp-msp1.png)

Le diagramme suivant illustre la progression d’un appel entrant qui implique à la fois un TSP et un MSP.

![appel entrant avec un TSP et un MSP](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Configuration de l’appel entrant

-   Le TSP envoie un message de [**ligne \_ NEWCALL**](line-newcall.md) à tapisrv. L' [**État**](./linecallstate--constants.md) de l’appel est LINECALLSTATE \_ .
-   TAPISRV notifie les clients de l’appel.
-   TAPI3 crée l’objet d’appel TAPI, puis appelle [**ITMSPAddress :: CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), qui est implémenté par le MSP.
-   Le MSP crée un objet d’appel MSP et des flux par défaut en fonction des [**types de médias**](./tapimediatype--constants.md) requis pour l’appel. Elle retourne un pointeur IUnknown vers l’objet d’appel MSP.
-   TAPI3 agrège l’objet d’appel MSP dans l’objet d’appel TAPI, ce qui rend les interfaces telles que [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) disponibles pour l’application. Il avertit ensuite l’application du nouvel appel.

L’application peut ensuite utiliser des méthodes telles que [**ITStream :: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) pour terminer les préparatifs de la fin de l’appel.

## <a name="incoming-call-completion"></a>Fin de l’appel entrant

-   L’application appelle [**ITBasicCallControl :: Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 appelle [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV appelle [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   Le TSP lance la diffusion en continu des appels. En règle générale, le TSP envoie un message au MSP correspondant, et le MSP démarre les flux. Dans certaines implémentations de TSP/MSP, le TSP démarre les flux.

## <a name="tspmsp-communication-during-call-progress"></a>Communication TSP/MSP pendant la progression de l’appel

Une fois l’appel en cours, le TSP et le MSP communiquent en passant les mémoires tampon opaques via TAPISRV et TAPI3.

-   Le TSP envoie des informations au MSP en envoyant la [**ligne \_ SENDMSPDATA**](line-sendmspdata.md) message à tapisrv.
-   Le MSP reçoit des informations du TSP via la méthode [**ITMSPAddress :: ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) . Si les données sont associées à un objet d’appel MSP, un pointeur d’interface vers l’objet d’appel MSP est fourni en tant que paramètre de cette méthode.
-   Le MSP envoie des informations au TSP en envoyant un \_ événement de \_ données MSP du TSP à TAPI 3.
-   Le TSP reçoit des informations du MSP via la fonction [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) .

Le processus et le contenu exacts de la communication entre les fournisseurs de services sont spécifiques à un TSP/MSP donné.

> [!Note]  
> Pour les appels sortants, le MSP connaît généralement l’appel avant le TSP. Si le MSP tente de communiquer avec le TSP avant que le TSP soit informé d’un appel, la communication échoue. Lorsque le MSP et le TSP doivent échanger des informations concernant un appel spécifique, le TSP doit lancer la communication.

 

 

 
