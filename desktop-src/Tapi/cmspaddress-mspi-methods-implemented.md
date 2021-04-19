---
description: Voici les méthodes MSPI standard que tous les MSP doivent implémenter. La documentation principale pour ces méthodes existe dans la section de référence sur l’interface MSPI (Media Service Provider Interface).
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: Méthodes CMSPAddress MSPI implémentées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed19bbacc13990d052c35bda68f97db80ff68ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538713"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>Méthodes CMSPAddress MSPI implémentées

Voici les méthodes MSPI standard que tous les MSP doivent implémenter. La documentation principale pour ces méthodes existe dans la section de référence sur l' [interface MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md) .



| Méthodes CMSPAddress                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Initialiser**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Appelée par TAPI3 lorsque ce MSP est créé pour la première fois.                                                                                                                                                                                                                                                                                                   |
| [**Correct**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Appelée par TAPI3 lorsque cette adresse n’est plus utilisée.                                                                                                                                                                                                                                                                                         |
| [**ReceiveTSPData**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Appelée par TAPI3 lorsque le TSP envoie des données à cet objet d’adresse MSP.                                                                                                                                                                                                                                                                               |
| [**GetEvent**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Appelée par TAPI3 pour obtenir des informations détaillées sur un événement.                                                                                                                                                                                                                                                                                       |
| [**Obtient \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper OLE Automation pour la fonction d’assistance [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                            |
| [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper d’énumération pour la fonction d’assistance [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                               |
| [**Obtient \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper OLE Automation pour la fonction d’assistance [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                              |
| [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper d’énumération pour la fonction d’assistance [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                                 |
| [**CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Cette méthode est appelée par l’application pour créer un terminal dynamique. Il planifie un élément de travail sur le thread de travail du MSP, qui, lorsqu’il est exécuté, demande au gestionnaire de terminaux de créer un terminal dynamique. La classe dérivée peut substituer cette méthode pour avoir sa propre façon de créer un terminal dynamique.                                |
| [**GetDefaultStaticTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Cette méthode est appelée par l’application pour obtenir le terminal statique par défaut pour un type et une direction spécifiés. Il met à jour la liste des terminaux par défaut (si nécessaire) et retourne le pointeur d’interface. La classe dérivée peut substituer cette méthode pour avoir sa propre façon de déterminer quel terminal est la valeur par défaut. Verrouille les listes de terminaux. |



 

 

 
