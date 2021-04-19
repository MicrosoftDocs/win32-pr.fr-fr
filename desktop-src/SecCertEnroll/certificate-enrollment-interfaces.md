---
description: Les interfaces suivantes peuvent être utilisées pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522443"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="ba4b2-103">Interfaces d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="ba4b2-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="ba4b2-104">Les interfaces suivantes peuvent être utilisées pour inscrire un utilisateur ou un ordinateur dans une hiérarchie de certificats.</span><span class="sxs-lookup"><span data-stu-id="ba4b2-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="ba4b2-105">Interface</span><span class="sxs-lookup"><span data-stu-id="ba4b2-105">Interface</span></span>                                              | <span data-ttu-id="ba4b2-106">Description</span><span class="sxs-lookup"><span data-stu-id="ba4b2-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba4b2-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="ba4b2-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="ba4b2-108">Inscrit un ordinateur ou un utilisateur dans une hiérarchie de certificats.</span><span class="sxs-lookup"><span data-stu-id="ba4b2-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="ba4b2-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="ba4b2-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="ba4b2-110">Étend l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour permettre l’initialisation à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="ba4b2-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="ba4b2-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="ba4b2-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="ba4b2-112">Définit des méthodes qui permettent à une application Web d’inscrire un certificat, de stocker des informations d’identification de serveur de stratégie dans le cache des informations d’identification et d’inscrire des serveurs de stratégie et des serveurs d’inscription.</span><span class="sxs-lookup"><span data-stu-id="ba4b2-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="ba4b2-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="ba4b2-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="ba4b2-114">Récupère des informations d’erreur détaillées sur une transaction d’inscription de certificat.</span><span class="sxs-lookup"><span data-stu-id="ba4b2-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="ba4b2-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="ba4b2-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="ba4b2-116">Interface du protocole d’inscription d’ordinateur simple X. 509</span><span class="sxs-lookup"><span data-stu-id="ba4b2-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ba4b2-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba4b2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4b2-118">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="ba4b2-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




