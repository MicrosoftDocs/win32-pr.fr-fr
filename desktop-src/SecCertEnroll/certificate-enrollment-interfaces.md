---
description: Les interfaces suivantes peuvent être utilisées pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb71c1240791e26781797b547b0a62aaad1612a2bce06738cecfa02c8173b215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902740"
---
# <a name="certificate-enrollment-interfaces"></a>Interfaces d’inscription de certificats

Les interfaces suivantes peuvent être utilisées pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.



| Interface                                              | Description                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Inscrit un ordinateur ou un utilisateur dans une hiérarchie de certificats.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Étend l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour permettre l’initialisation à partir d’un modèle.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Définit des méthodes qui permettent à une application Web d’inscrire un certificat, de stocker des informations d’identification de serveur de stratégie dans le cache des informations d’identification et d’inscrire des serveurs de stratégie et des serveurs d’inscription. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Récupère des informations d’erreur détaillées sur une transaction d’inscription de certificat.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Interface du protocole d’inscription d’ordinateur simple X. 509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 




