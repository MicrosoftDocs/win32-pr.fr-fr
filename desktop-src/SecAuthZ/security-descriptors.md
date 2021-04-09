---
description: Un descripteur de sécurité contient les informations de sécurité associées à un objet sécurisable.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descripteurs de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863006"
---
# <a name="security-descriptors"></a><span data-ttu-id="f16b8-103">Descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="f16b8-103">Security Descriptors</span></span>

<span data-ttu-id="f16b8-104">Un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) contient les informations de sécurité associées à un [objet sécurisable](securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f16b8-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="f16b8-105">Un descripteur de sécurité se compose d’une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) et des informations de sécurité qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="f16b8-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="f16b8-106">Un descripteur de sécurité peut inclure les informations de sécurité suivantes :</span><span class="sxs-lookup"><span data-stu-id="f16b8-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="f16b8-107">[Identificateurs de sécurité](security-identifiers.md) (SID) pour le propriétaire et le groupe principal d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f16b8-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="f16b8-108">[Liste DACL](access-control-lists.md) qui spécifie les droits d’accès accordés ou refusés à des utilisateurs ou des groupes particuliers.</span><span class="sxs-lookup"><span data-stu-id="f16b8-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="f16b8-109">[SACL](access-control-lists.md) qui spécifie les types de tentatives d’accès qui génèrent des enregistrements d’audit pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="f16b8-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="f16b8-110">Ensemble de bits de contrôle qui qualifient la signification d’un descripteur de sécurité ou de ses membres individuels.</span><span class="sxs-lookup"><span data-stu-id="f16b8-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="f16b8-111">Les applications ne doivent pas manipuler directement le contenu d’un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f16b8-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="f16b8-112">L’API Windows fournit des fonctions permettant de définir et de récupérer les informations de sécurité dans le descripteur de sécurité d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f16b8-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="f16b8-113">En outre, il existe des fonctions permettant de créer et d’initialiser un descripteur de sécurité pour un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="f16b8-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="f16b8-114">Les applications qui utilisent des descripteurs de sécurité sur des objets Active Directory peuvent utiliser les fonctions de sécurité Windows ou les interfaces de sécurité fournies par les interfaces de service Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="f16b8-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="f16b8-115">Pour plus d’informations sur les interfaces de sécurité ADSI, consultez fonctionnement [de Access Control dans Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="f16b8-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
