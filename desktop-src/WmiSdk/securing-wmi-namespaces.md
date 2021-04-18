---
description: L’accès aux espaces de noms WMI et à leurs données est contrôlé par les descripteurs de sécurité.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Sécurisation des espaces de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519020"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="ea0f5-103">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="ea0f5-104">L’accès aux espaces de noms WMI et à leurs données est contrôlé par les [*descripteurs de sécurité*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="ea0f5-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="ea0f5-105">Vous pouvez protéger les données de vos [*espaces de noms*](gloss-n.md) en ajustant le descripteur de sécurité de l’espace de noms pour contrôler qui a accès aux données et aux méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="ea0f5-106">Pour plus d’informations, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ea0f5-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="ea0f5-107">Les rubriques suivantes décrivent la sécurité de l’espace de noms WMI et expliquent comment contrôler l’accès aux espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="ea0f5-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="ea0f5-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="ea0f5-109">La sécurité des espaces de noms WMI repose sur des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) d’utilisateur Windows standard et des listes de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="ea0f5-110">Les administrateurs et les utilisateurs ont des autorisations par défaut différentes.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f5-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="ea0f5-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="ea0f5-112">Une fois qu’un espace de noms existe dans le référentiel WMI, vous pouvez modifier la sécurité de l’espace de noms à l’aide du contrôle WMI ou en appelant les méthodes de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ea0f5-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea0f5-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ea0f5-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="ea0f5-114">Le qualificateur **RequiresEncryption** sur un espace de noms exige que le script ou l’application cliente WMI utilise le niveau d’authentification qui chiffre les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="ea0f5-115">Les demandes de données entrantes et les rappels asynchrones doivent être chiffrés.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f5-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Établissement de l’héritage de la sécurité des espaces de noms](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="ea0f5-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="ea0f5-117">Vous pouvez contrôler si un espace de noms enfant hérite du descripteur de sécurité de l’espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="ea0f5-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ea0f5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea0f5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f5-119">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="ea0f5-120">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="ea0f5-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="ea0f5-121">Création d’un espace de noms avec l’API WMI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="ea0f5-122">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="ea0f5-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
