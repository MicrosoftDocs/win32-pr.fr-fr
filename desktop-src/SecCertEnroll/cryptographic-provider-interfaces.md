---
description: Les interfaces suivantes peuvent être utilisées pour récupérer des informations sur les fournisseurs de chiffrement.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfaces du fournisseur de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e39e42f17efdeae353b02723522e744031a394e8faa8a4be986831087561e4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976909"
---
# <a name="cryptographic-provider-interfaces"></a>Interfaces du fournisseur de services de chiffrement

Les interfaces suivantes peuvent être utilisées pour récupérer des informations sur les fournisseurs de chiffrement.



| Interface                                    | Description                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | Représente un algorithme implémenté par un fournisseur de services de chiffrement.             |
| [**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | Gère une collection d’objets [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) . |
| [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | Donne accès à des informations générales sur un fournisseur de services de chiffrement.       |
| [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | Gère une collection d’objets [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .  |
| [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | Contient des informations sur une paire fournisseur/algorithme de chiffrement.          |
| [**ICspStatuses**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | Gère une collection d’objets [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



