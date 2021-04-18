---
description: 'Les fonctions suivantes sont utilisées lors de l’utilisation d’enclaves utilisées pour créer des environnements d’exécution approuvés :'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Fonctions d’exécution approuvées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516285"
---
# <a name="trusted-execution-functions"></a>Fonctions d’exécution approuvées

Les fonctions suivantes sont utilisées lors de l’utilisation d’enclaves utilisées pour créer des environnements d’exécution approuvés :

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                               | Description                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Appelle une fonction au sein d’une enclave. <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Crée une enclave non initialisée. Une enclave est une région isolée de code et des données dans l’espace d’adressage d’une application. Seul le code qui s’exécute dans l’enclave peut accéder aux données dans la même enclave.<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Supprime l’enclave spécifiée.<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Obtient un rapport d’attestation d’enclave qui décrit l’enclave en cours et est signé par l’autorité responsable du type de l’enclave. <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Obtient des informations sur l’enclave en cours d’exécution.<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Génère un objet BLOB (Binary Large Object) chiffré à partir de données unencypted.<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Déchiffre un objet BLOB (Binary Large Object) chiffré.<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Vérifie un rapport d’attestation qui a été généré sur le système actuel. <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Initialise une enclave que vous avez créée et chargée avec des données.<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Récupère une valeur indiquant si le type spécifié d’enclave est pris en charge.<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Charge des données dans une enclave non initialisée que vous avez créée en appelant [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave).<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Charge une image et toutes ses importations dans une enclave.<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Met fin à l’exécution des threads qui s’exécutent dans une enclave.<br/>                                                                                                                                               |



 

 

 




