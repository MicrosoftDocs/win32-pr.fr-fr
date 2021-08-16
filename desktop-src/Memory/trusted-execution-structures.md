---
description: 'Les structures suivantes sont utilisées lors de l’utilisation d’enclaves utilisées pour créer des environnements d’exécution approuvés :'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Structures d’exécution approuvées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386250"
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
| [**CONFIG32 de l’enclave d’IMAGE \_ \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Définit le format de la configuration de l’enclave pour les systèmes qui exécutent des Windows bits 32.<br/>                                                                                                                                          |
| [**CONFIG64 de l’enclave d’IMAGE \_ \_**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Définit le format de la configuration de l’enclave pour les systèmes qui exécutent des Windows bits 64.<br/>                                                                                                                                          |
| [**importation d’une enclave d’images \_ \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Définit une entrée dans le tableau d’images qu’une enclave peut importer.<br/>                                                                                                                                                           |
| [**\_rapport d’enclaves vbs \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Décrit le format de l’instruction signée contenue dans un rapport généré en appelant la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_module de rapport d’enclaves vbs \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Décrit un module chargé pour l’enclave.<br/>                                                                                                                                                                                   |
| [**VBS \_ \_ \_ \_ -en-tête pkg du rapport d’enclave**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Décrit le contenu d’un rapport généré en appelant la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**VBS \_ enclave \_ \_ \_ -en-tête VARDATA**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Décrit le format d’un bloc de données de variable contenu dans un rapport généré par la fonction [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
