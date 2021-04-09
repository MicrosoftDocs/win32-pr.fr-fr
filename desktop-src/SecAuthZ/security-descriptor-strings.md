---
description: Un descripteur de sécurité fonctionnel valide contient des informations de sécurité au format binaire.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Chaînes de descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113786"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="37040-103">Chaînes de descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="37040-103">Security Descriptor Strings</span></span>

<span data-ttu-id="37040-104">Un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) fonctionnel valide contient des informations de sécurité au format binaire.</span><span class="sxs-lookup"><span data-stu-id="37040-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="37040-105">L’API Windows fournit des fonctions permettant de convertir des descripteurs de sécurité binaires vers et à partir de chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="37040-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="37040-106">Les descripteurs de sécurité au format chaîne ne sont pas fonctionnels, mais ils peuvent être utiles pour stocker ou transporter des informations de descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37040-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="37040-107">Pour convertir un descripteur de sécurité en un format de chaîne, appelez la fonction [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="37040-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="37040-108">Pour convertir un descripteur de sécurité au format chaîne en un descripteur de sécurité fonctionnel valide, appelez la fonction [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="37040-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="37040-109">Pour plus d’informations, consultez [langage de définition du descripteur de sécurité](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="37040-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
