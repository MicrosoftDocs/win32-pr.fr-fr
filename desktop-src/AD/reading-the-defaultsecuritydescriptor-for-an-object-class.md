---
title: Lecture du defaultSecurityDescriptor pour une classe d’objet
description: À l’aide d’ADSI, vous pouvez obtenir l’attribut defaultSecurityDescriptor pour une classe d’objet à l’aide de l’interface IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, lecture du defaultSecurityDescriptor pour une classe d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030988"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="3a2a3-104">Lecture du defaultSecurityDescriptor pour une classe d’objet</span><span class="sxs-lookup"><span data-stu-id="3a2a3-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="3a2a3-105">À l’aide d’ADSI, vous pouvez obtenir l’attribut **defaultSecurityDescriptor** pour une classe d’objet à l’aide de l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="3a2a3-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="3a2a3-106">Pour obtenir l’attribut **defaultSecurityDescriptor** pour une classe d’objet, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="3a2a3-107">Obtient un pointeur d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) vers l’objet **classSchema** pour la classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="3a2a3-108">Utilisez la méthode [**IADs. obten**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le descripteur de sécurité par défaut de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="3a2a3-109">Le nom de la propriété qui contient le descripteur de sécurité est « defaultSecurityDescriptor ».</span><span class="sxs-lookup"><span data-stu-id="3a2a3-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="3a2a3-110">La propriété est retournée en tant que [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contenant un BSTR avec le descripteur de sécurité par défaut au format de chaîne SDDL.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="3a2a3-111">Utilisez la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) pour convertir le format de chaîne SDDL en descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="3a2a3-112">Utilisez les API de sécurité [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)et [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) pour lire les parties du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3a2a3-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="3a2a3-113">Pour obtenir un exemple de code qui montre comment procéder, consultez l' [exemple de code pour la lecture de defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="3a2a3-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 