---
description: L’opération de collecte permet à une application de répondre à une session qui alerte à une autre adresse. L’application identifie la cible de la collecte et retourne un identificateur de session pour l’appel prélevé.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Collecte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758337"
---
# <a name="pickup"></a>Collecte

L’opération de collecte permet à une application de répondre à une session qui alerte à une autre adresse. L’application identifie la cible de la collecte et retourne un identificateur de session pour l’appel prélevé.

Il existe plusieurs façons d’identifier la cible de la demande de cueillette. Tout d’abord, l’application peut spécifier l’adresse du tiers d’alertes. Deuxièmement, si aucune adresse n’est spécifiée et que le commutateur l’autorise, l’application peut récupérer toute session d’alerte dans son groupe de collecte. Troisièmement, certains commutateurs autorisent la collecte d’une alerte de session dans un groupe de collecte différent si l’identificateur de groupe est spécifié.

Certains systèmes téléphoniques clés prennent en charge un *transfert par le biais* de la fonctionnalité de conservation des apparences d’appel exclusives de Bridge. Dans ce schéma, un téléphone particulier possède un appel exclusivement lorsque l’appel est actif, mais lorsque l’appel est en attente, tout téléphone ayant l’apparence de la ligne peut reprendre l’appel.

**TAPI 2. x :** Une application peut utiliser une opération de collecte avec une adresse cible **null** à cet effet, similaire à la façon dont la fonction est utilisée pour récupérer un appel d’appel en attente sur une ligne analogique. LINEADDRFEATURE \_ PICKUPHELD indique l’existence de la fonctionnalité.

Si LINEADDRCAPFLAGS \_ PICKUPCALLWAIT a la **valeur true**, une session peut être récupérée pour laquelle l’utilisateur a détecté de façon audible le signal d’appel en attente, mais pour lequel le fournisseur de services ne parvient pas à effectuer la détection. Cela donne à l’utilisateur un mécanisme pour « répondre » à un appel en attente, même si le fournisseur de services n’a pas pu détecter le signal d’appel-attente. L’adresse de destination et l’ID de groupe doivent tous deux avoir la **valeur null** pour récupérer un appel en attente d’appel.

Lorsqu’une session a été récupérée avec succès, l’application reçoit une notification de changement d’État avec la [raison](reason-ovr.md) définie sur LINECALLREASON \_ Pickup.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3. x :** Consultez [**ITBasicCallControl ::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
