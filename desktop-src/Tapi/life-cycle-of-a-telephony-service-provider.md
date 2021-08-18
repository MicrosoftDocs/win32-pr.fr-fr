---
description: Cette rubrique fournit une vue d’ensemble des opérations du TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Cycle de vie d’un fournisseur de services de téléphonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012697"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Cycle de vie d’un fournisseur de services de téléphonie

Cette rubrique fournit une vue d’ensemble des opérations du TSP.

Une session est le temps pendant lequel une configuration particulière reste valide et les opérations de téléphonie sont effectuées. Un fournisseur de services peut prendre en charge de nombreuses sessions entre le moment où il est chargé pour la première fois et le moment où il est enfin libéré. Pour chaque session, TAPI négocie la version de l’interface, démarre la session, effectue les opérations et finit par arrêter la session. Le fournisseur de services ne doit pas conserver les informations d’une session à la suivante.

Une fois la version de l’interface connue, TAPI appelle la fonction [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) pour définir tous les paramètres opérationnels. Le fournisseur de services s’assure que toutes les informations de configuration dans le Registre sont stables lorsque la fonction **TSPI \_ providerInit** est appelée. La plupart des fournisseurs de services lisent toutes les informations de configuration à ce moment-là.

Les opérations normales peuvent continuer dans n’importe quel ordre, après l’initialisation du fournisseur de services.

L’interface TAPI négocie les informations spécifiques à l’appareil sur la base de chaque appareil. L’interface TAPI et le fournisseur de services sont validés sur une version quand un appareil est ouvert.

Le fournisseur de services peut recevoir des demandes de sélection et d’annulation des versions d’extension. Alors qu’une version d’extension est sélectionnée, l’appareil fonctionne de façon stricte en fonction de la version d’extension propre à l’appareil.

La négociation d’une version d’extension spécifique à l’appareil peut se produire plusieurs fois, avant et après l’ouverture de l’appareil. TAPI passe une plage de versions, et le fournisseur de services choisit et retourne une valeur de cette plage. Normalement, les extensions spécifiques à l’appareil sont désactivées pour le fournisseur de services.

Cela permet de valider l’utilisation de l’interface TAPI et du fournisseur de services au niveau de la version de l’extension jusqu’à ce que la sélection soit annulée. Pendant la durée pendant laquelle une extension spécifique à l’appareil est en vigueur, une tentative de négociation d’un niveau de version d’extension doit autoriser uniquement le niveau de version qui est actuellement en vigueur. Une fois l’extension spécifique à l’appareil annulée, une version différente peut être négociée et sélectionnée.

les opérations de Téléphone au sein de la paire **ouverture/fermeture** sont présentées dans l’illustration suivante. Certaines de ces opérations sont synchrones, d’autres sont asynchrones. Si une opération se termine de façon asynchrone, une autre opération peut être demandée avant la fin du premier rapport. Ainsi, les opérations peuvent se chevaucher de quelque manière que ce soit. Le fournisseur de services doit finalement signaler l’achèvement de toute opération asynchrone demandée. La fermeture d’un téléphone force l’exécution des opérations asynchrones en suspens (éventuellement avec une indication « échec »).

Le cycle de vie des appareils en ligne est similaire au cycle de vie des téléphones, à ceci près que les lignes ont leurs propres procédures de négociation, d’initialisation, d’ouverture et de fermeture. Les opérations sur les lignes ouvertes sont placées entre crochets par leur propre paire **ouvrir/fermer** . Cette paire est à son tour comprise entre la même paire **d’initialisation et d’arrêt** que le téléphone **ouvrir/fermer**.

Les cycles de vie des appels sont limités de façon stricte entre l' **ouverture et la fermeture** de la ligne qui les contient. Les durées de vie des appels peuvent commencer de plusieurs façons :

-   Demandé à partir de l’interface TAPI via des fonctions telles que [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)ou [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference).
-   Est à l’origine spontanée du fournisseur de services en tant que nouveaux appels entrants, appels initiés par l’utilisateur sur un téléphone connecté ou appels générés en tant qu’effet secondaire d’autres opérations, telles que l’exécution d’un appel existant en attente.

Les durées de vie des appels distincts au sein de la même ligne peuvent se chevaucher de quelque manière que ce soit. Tous les appels terminent leur durée de vie au moment où la fonction TSPI [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) est appelée. Le cycle de vie de plusieurs appels est illustré dans l’illustration suivante.

![cycles de vie des appels se chevauchant](images/modell.png)

Un appel peut provenir de l’interface TAPI, comme indiqué avec la paire **MakeCall/CloseCall** . Un appel peut également provenir du fournisseur de services. Le fournisseur de services annonce cela avec un message de [**ligne \_ NEWCALL**](line-newcall.md) à une procédure de rappel fournie par TAPI. Dans ce cas, l’interface TAPI retourne son identificateur pour l’appel, qui est inclus dans les rappels suivants signalant des événements qui se produisent lors de l’appel. Dans le cas d’appels dont la durée de vie provient de TAPI, cet identificateur est inclus dans l’opération TSPI qui crée l’appel.

Toutes les opérations qui démarrent la durée de vie d’un appel entraînent l’échange d’identificateurs pour le nouvel appel par l’interface TAPI et le fournisseur de services. Dans le cas d’appels émis par TAPI, TAPI passe son identificateur et reçoit l’identificateur du fournisseur de services en tant que paramètre de retour. Dans le cas où l’appel provient du fournisseur de services, le fournisseur de services passe son identificateur à l’interface TAPI et reçoit l’identificateur TAPI en tant que paramètre de retour.

L’illustration suivante offre une vue d’ensemble générale de l’installation, de la configuration et de la suppression du fournisseur de services. séquences de cycle de vie qui s’étendent sur de nombreuses sessions. Le cycle de vie classique de ces opérations peut être affiché avec la chronologie suivante.

![installation, configuration et suppression du fournisseur de services](images/model2.png)

Le cycle de vie d’installation et de suppression classique s’affiche, couvrant plusieurs sessions. Les appels aux procédures d' **installation** et de [**suppression**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) sont strictement couplés et ne se chevauchent pas. Les appels à la procédure de **configuration** peuvent se produire plusieurs fois dans cette paire. L’une est généralement effectuée par le fournisseur de services en tant qu’effet secondaire interne de la procédure d' **installation** pour créer des entrées de ligne et de téléphone. La procédure de **configuration** peut être appelée à d’autres moments pour modifier une configuration existante. La procédure d' **installation** doit être effectuée avant que toute autre fonction TSPI ne soit autorisée. Dans le scénario idéal, toutes les sessions sont strictement imbriquées dans la paire de procédures d' **installation/suppression** .

Les fonctions [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)et [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagissent avec le fournisseur de services lui-même plutôt qu’avec un appareil spécifique. Elles affectent les informations de configuration statiques qui subsistent sur plusieurs sessions et doivent être présentes pour que toute autre opération continue. Ainsi, toutes les autres opérations sont imbriquées entre l’appel de **TSPI \_ providerInstall** et l’achèvement de son **\_ providerRemove TSPI** correspondant. Ces deux opérations se produisent généralement très éloignées, le plus souvent dans une charge différente du fournisseur de services ou un autre démarrage de l’ordinateur. L’appel de la fonction de **configuration** en externe est facultatif, car la procédure d' **installation** est nécessaire pour inclure le comportement de **configuration** en plus de son propre. La raison habituelle de l’appeler en externe consiste à modifier une configuration existante.

Une subtilité est incorporée dans le concept de l’achèvement d’une opération [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) . Il est souhaitable de permettre à l’utilisateur d’exécuter l’utilitaire du panneau de configuration de la téléphonie fourni avec le service de téléphonie pour modifier les configurations du fournisseur de services, même lorsque des opérations de téléphonie (sessions) sont en cours. Par conséquent, les spécifications [**TSPI \_ ProviderConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) et **TSPI \_ providerRemove** autorisent l’appel pendant qu’une session est en attente. Toutefois, toute modification apportée à la configuration doit être retardée jusqu’à ce que les opérations de téléphonie soient arrêtées et redémarrées. Ainsi, strictement parlant, l’achèvement de toute opération **TSPI \_ ProviderConfig** ou **TSPI \_ providerRemove** se produit en dehors de toute session. L’imbrication des actions est indiquée dans la figure, même si les appels de procédures peuvent apparaître dans un ordre légèrement différent. Il est permis à un fournisseur de services d’interdire simplement la **configuration** ou la [**suppression**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) pendant que les opérations sont en cours, même si l’utilisateur doit être averti avec une boîte de dialogue. Une implémentation plus conviviale qui permet au moins un sous-ensemble d’opérations est préférable.

Ces opérations d' **installation**, de **configuration** et de [**suppression**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) ont toutes l’effet secondaire de signaler les applications de téléphonie en cours d’exécution, ce qui finit par entraîner l’arrêt de l’utilisation du service de téléphonie. Ensemble, cela met fin à toutes les sessions en suspens pour les fournisseurs de services. Cela signifie aux fournisseurs de services qu’ils doivent lire la nouvelle configuration du registre lorsque de nouvelles sessions commencent. Toutes les modifications en attente en raison d’une **configuration** ou d’une [**suppression**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) alors que des opérations étaient en cours prennent effet.

 

 
