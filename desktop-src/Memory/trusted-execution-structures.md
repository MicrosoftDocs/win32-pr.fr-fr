---
description: 'Les structures suivantes sont utilisées lors de l’utilisation d’enclaves utilisées pour créer des environnements d’exécution approuvés :'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Structures d’exécution approuvées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524179"
---
# <a name="trusted-execution-structures"></a>Structures d’exécution approuvées

Les structures suivantes sont utilisées lors de l’utilisation d’enclaves utilisées pour créer des environnements d’exécution approuvés :

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                         | Description                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE- \_ créer \_ info \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contient des informations spécifiques à l’architecture à utiliser pour créer une enclave lorsque le type de l’enclave est l' **enclave \_ type \_ SGX**, qui spécifie une enclave pour l’extension d’architecture Intel Software Guard extensions (SGX).<br/>     |
| [**ENCLAVE- \_ créer des \_ informations \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contient des informations spécifiques à l’architecture à utiliser pour créer une enclave lorsque le type de l’enclave est le **type d’enclave \_ \_ vbs**, qui spécifie une enclave de sécurité basée sur la virtualisation (VBS).<br/>                                       |
| [**identité de l’ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Décrit l’identité du module principal d’une enclave. <br/>                                                                                                                                                                 |
| [**\_informations sur l’enclave**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contient des informations sur l’enclave en cours d’exécution.<br/>                                                                                                                                                                  |
| [**ENCLAVE \_ init \_ info \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contient des informations spécifiques à l’architecture à utiliser pour initialiser une enclave lorsque le type de l’enclave est l' **enclave \_ type \_ SGX**, qui spécifie une enclave pour l’extension d’architecture Intel Software Guard extensions (SGX).<br/> |
| [**ENCLAVE \_ init \_ info \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contient des informations spécifiques à l’architecture à utiliser pour initialiser une enclave lorsque le type de l’enclave est le **type d’enclave \_ \_ vbs**, qui spécifie une enclave de sécurité basée sur la virtualisation (VBS).<br/>                                   |
| [**CONFIG32 de l’enclave d’IMAGE \_ \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Définit le format de la configuration de l’enclave pour les systèmes exécutant Windows 32 bits.<br/>                                                                                                                                          |
| [**CONFIG64 de l’enclave d’IMAGE \_ \_**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Définit le format de la configuration de l’enclave pour les systèmes exécutant Windows 64 bits.<br/>                                                                                                                                          |
| [**importation d’une enclave d’images \_ \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Définit une entrée dans le tableau d’images qu’une enclave peut importer.<br/>                                                                                                                                                           |
| [**\_rapport d’enclaves vbs \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Décrit le format de l’instruction signée contenue dans un rapport généré en appelant la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_module de rapport d’enclaves vbs \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Décrit un module chargé pour l’enclave.<br/>                                                                                                                                                                                   |
| [**VBS \_ \_ \_ \_ -en-tête pkg du rapport d’enclave**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Décrit le contenu d’un rapport généré en appelant la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**VBS \_ enclave \_ \_ \_ -en-tête VARDATA**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Décrit le format d’un bloc de données de variable contenu dans un rapport généré par la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
