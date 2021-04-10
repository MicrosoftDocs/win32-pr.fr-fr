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
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lecture du defaultSecurityDescriptor pour une classe d’objet

À l’aide d’ADSI, vous pouvez obtenir l’attribut **defaultSecurityDescriptor** pour une classe d’objet à l’aide de l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) . Pour obtenir l’attribut **defaultSecurityDescriptor** pour une classe d’objet, procédez comme suit.

1.  Obtient un pointeur d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) vers l’objet **classSchema** pour la classe d’objet.
2.  Utilisez la méthode [**IADs. obten**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le descripteur de sécurité par défaut de l’objet. Le nom de la propriété qui contient le descripteur de sécurité est « defaultSecurityDescriptor ». La propriété est retournée en tant que [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contenant un BSTR avec le descripteur de sécurité par défaut au format de chaîne SDDL.
3.  Utilisez la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) pour convertir le format de chaîne SDDL en descripteur de sécurité.
4.  Utilisez les API de sécurité [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)et [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) pour lire les parties du descripteur de sécurité.

Pour obtenir un exemple de code qui montre comment procéder, consultez l' [exemple de code pour la lecture de defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 