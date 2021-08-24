---
title: Fonctions du client de transport WDS
description: Ce module définit les structures et les fonctions qui composent l’interface entre le récepteur de contenu et le client de transport.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f228370aa0973e124b1877dcf8a458d1356170fbb872a05a1867ac0489c00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680399"
---
# <a name="wds-transport-client-functions"></a>Fonctions du client de transport WDS

Ce module définit les structures et les fonctions qui composent l’interface entre le récepteur de contenu et le client de transport.



| Fonction                                                                              | Description                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsTransportClientReceiveContents*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Indique qu’un bloc de données est prêt à être utilisé.                                                                                                                         |
| [*PFN \_ WdsTransportClientReceiveMetadata*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Reçoit des informations de métadonnées sur un fichier.                                                                                                                                 |
| [*PFN \_ WdsTransportClientSessionComplete*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Indique que la session s’est terminée correctement ou a rencontré une erreur.                                                                                                  |
| [*PFN \_ WdsTransportClientSessionStart*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Indique la taille du fichier et d’autres informations côté serveur sur le fichier au consommateur.                                                                                   |
| [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Indique la taille du fichier et d’autres informations côté serveur sur le fichier au consommateur.                                                                                   |
| [**WdsTransportClientAddRefBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Incrémente le décompte de références sur une mémoire tampon détenue par le client de multidiffusion.                                                                                                   |
| [**WdsTransportClientCancelSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Libère les ressources associées à une session dans le client.                                                                                                             |
| [**WdsTransportClientCloseSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Libère les ressources associées à une session dans le client.                                                                                                             |
| [**WdsTransportClientCompleteReceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Indique que tout le traitement d’un bloc de données est terminé et que le client de multidiffusion peut supprimer ce bloc de données de son cache pour libérer de l’espace pour les réceptions ultérieures. |
| [**WdsTransportClientInitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Initialise le client multicast.                                                                                                                                           |
| [**WdsTransportClientInitializeSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Lance un transfert de fichiers de multidiffusion.                                                                                                                                        |
| [**WdsTransportClientQueryStatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Récupère l’état actuel d’une transmission par multidiffusion en cours ou complète à partir du client de multidiffusion.                                                                    |
| [**WdsTransportClientRegisterCallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Inscrit un rappel auprès du client multicast.                                                                                                                             |
| [**WdsTransportClientReleaseBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Décrémente le décompte de références sur une mémoire tampon détenue par le client de multidiffusion.                                                                                                   |
| [**WdsTransportClientShutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Arrête le client de multidiffusion.                                                                                                                                            |
| [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Lance un transfert de fichiers de multidiffusion.                                                                                                                                        |
| [**WdsTransportClientWaitForCompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Bloque jusqu’à ce que la session de multidiffusion soit terminée ou que le délai d’attente spécifié soit atteint.                                                                                  |



 

 

 




