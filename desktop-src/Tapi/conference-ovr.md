---
description: La Conférence avancée utilisant des réseaux IP est décrite dans TAPI 3S Rendezvous IP Telephony Conferencing. Les éléments suivants concernent la Conférence de base.
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: Salles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518343"
---
# <a name="conference"></a>Salles

La Conférence avancée utilisant des réseaux IP est décrite dans la Conférence de [téléphonie IP Rendezvous](rendezvous-ip-telephony-conferencing.md)de l’interface TAPI 3. Les éléments suivants concernent la Conférence de base.

Les sessions de conférence sont des sessions qui incluent plus de deux parties simultanément. Ils peuvent être configurés à l’aide d’un pont externe basé sur un serveur ou d’un pont de conférence basé sur un commutateur.

Dans les sessions de conférence basées sur le serveur, toutes les parties participantes se connectent au serveur, qui combine les flux de médias et envoie chaque participant à la combinaison. Il se peut qu’il n’y ait aucune notion de tiers dans l’appel de conférence, uniquement celle d’un appel unique entre l’application et le serveur de pont. Pour l’interface TAPI, ce type d’appel de conférence semble être une connexion un-à-un normale.

La Conférence basée sur les commutateurs s’exécute par étapes, dont certaines peuvent être combinées si le fournisseur de services le prend en charge :

1.  Lancez une session de communication ordinaire.
2.  Créez une session de conférence avec son premier membre le tiers qui a initié la Conférence.
3.  Créer une session de consultation de conférence avec le tiers à l’autre extrémité de la connexion actuelle.
4.  Ajoutez la session de consultation à la Conférence.

Une fois qu’une session devient membre d’une conférence, l’état du membre revient à la Conférence. L’état de la session de conférence est généralement *connecté*. Les identificateurs de session à la Conférence et toutes les parties ajoutées restent valides. Vous pouvez recevoir des événements d’État sur tous les appels. Par exemple, si l’un des membres se déconnecte en raccrochant, un message d’état approprié peut informer l’application de ce fait.

**TAPI 2. x :** Les applications peuvent utiliser la fonctionnalité « aucune conférence de blocage » des PBX à l’aide de l' \_ option LINECALLPARAMFLAGS NOHOLDCONFERENCE ; cette fonctionnalité permet à un autre appareil, tel qu’un superviseur ou un appareil d’enregistrement, d’être attaché en mode silencieux à la ligne.

Lors de l’annulation de la session de consultation auprès du tiers pour une conférence ou lors de la suppression du tiers dans une conférence précédemment établie, le fournisseur de services peut libérer la Conférence et rétablir la session à une connexion à deux tiers normale. Si c’est le cas, la session de conférence passera à l’état *inactif* et la seule session participante restante passera de la Conférence à l’état *connecté* .

Tous les fournisseurs de services ne prennent pas en charge la Conférence.

**TAPI 2. x :** La fonction [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) prend l’appel d’origine à deux tiers comme entrée, alloue un appel de conférence, connecte l’appel d’origine à la Conférence et alloue un appel de consultation dont le handle est retourné à l’application.

Si l’application va ajouter un autre membre à la Conférence, une opération de connexion peut être effectuée sur l’appel de consultation. Le handle de l’appel de conférence et la connexion d’appel de consultation sont ensuite utilisés dans la fonction [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) . Les membres d’une conférence peuvent également être ajoutés à l’aide de la fonction [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) , si elle est prise en charge par le fournisseur de services.

Les membres de la Conférence sont supprimés à l’aide de la fonction [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) , si le fournisseur de services le prend en charge.

Une conférence peut également être créée à l’aide de la fonction [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) , qui retourne un descripteur d’appel de consultation et la fonction [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) avec l’option de conférence (au lieu de l’option de [transfert](transfer-ovr.md) ).

**TAPI 3. x :** La méthode [**ITBasicCallControl :: Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) prend la session existante comme entrée et crée un [objet CallHub](callhub-object.md) s’il n’en existe pas déjà une. La méthode [**ITBasicCallControl :: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) ajoute l’appel de consultation à CallHub. Des sessions de consultation supplémentaires peuvent être créées à l’aide de [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)et ajoutées à l’aide des méthodes **Conference** et **Finish** .

> [!Note]  
> Les fonctionnalités de l’appareil de ligne de conduite peuvent limiter le nombre de parties participant à un appel unique et indiquer si une conférence commence ou non par un appel normal à deux parties.

 

 

 
