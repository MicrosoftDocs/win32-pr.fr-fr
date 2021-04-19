---
description: La liste suivante répertorie les qualificateurs standard spécifiques à WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificateurs WMI standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534619"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="7e0e6-103">Qualificateurs WMI standard</span><span class="sxs-lookup"><span data-stu-id="7e0e6-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="7e0e6-104">La liste suivante répertorie les qualificateurs standard spécifiques à WMI.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="7e0e6-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendement**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-106">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-106">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-107">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-107">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-108">Indique qu’une classe contient des qualificateurs modifiés qui sont localisés.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="7e0e6-109">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-109">The default is **TRUE**.</span></span>

<span data-ttu-id="7e0e6-110">La classe associée peut être traduite.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-110">The associated class can be translated.</span></span> <span data-ttu-id="7e0e6-111">Pour accéder à la version traduite, utilisez l’identificateur de paramètres régionaux pour construire un nom d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Ignorer \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-113">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-114">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-114">Applies to: methods</span></span>

<span data-ttu-id="7e0e6-115">Indique que l’appel de méthode doit passer directement à l’appel **ExecMethodAsync** du fournisseur plutôt qu’au fournisseur en appelant d’abord un appel à **GetObject** pour valider le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="7e0e6-116">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-116">The default is **FALSE**.</span></span> <span data-ttu-id="7e0e6-117">L’utilisation de la fonction de **contournement \_ GetObject** peut améliorer considérablement les performances.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="7e0e6-118">Avant d’utiliser le **contournement de \_ GetObject**, assurez-vous qu’aucune des actions suivantes n’est effectuée :</span><span class="sxs-lookup"><span data-stu-id="7e0e6-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="7e0e6-119">Dérivez une classe de votre classe.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="7e0e6-120">Substituez la méthode qui a le **qualificateur \_ GetObject Bypass** .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="7e0e6-121">L’échec de ces précautions peut entraîner l’appel de l’implémentation de la méthode de la classe parente au lieu de la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="7e0e6-122">Pour plus d’informations, consultez Utilisation du \_ qualificateur GetObject de contournement.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Clé CIM**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-124">Type de données **: \_ valeur booléenne CIM**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="7e0e6-125">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="7e0e6-125">Applies to: properties</span></span>

<span data-ttu-id="7e0e6-126">Indique que la propriété associée est une propriété de clé dans CIM, mais pas dans WMI.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-128">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-129">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="7e0e6-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="7e0e6-130">Contient le texte décrivant le type d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-132">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-133">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-133">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-134">Indique qu’une classe a des instances associées à plus d’informations fournies dynamiquement par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Déconseillé**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-136">Type de données **: \_ valeur booléenne CIM**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="7e0e6-137">S’applique à : Properties, classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-137">Applies to: properties, classes</span></span>

<span data-ttu-id="7e0e6-138">Indique que la propriété a été remplacée par une autre propriété.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Vidéo**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-140">S’applique à : classes, propriétés</span><span class="sxs-lookup"><span data-stu-id="7e0e6-140">Applies to: classes, properties</span></span>

<span data-ttu-id="7e0e6-141">**UUID** de la classe associée.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamique**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-143">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-144">S’applique à : classes, propriétés</span><span class="sxs-lookup"><span data-stu-id="7e0e6-144">Applies to: classes, properties</span></span>

<span data-ttu-id="7e0e6-145">Indique une classe dont les instances sont créées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="7e0e6-146">La valeur de ce qualificateur doit être définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-148">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-149">S’applique à : classes, instances</span><span class="sxs-lookup"><span data-stu-id="7e0e6-149">Applies to: classes, instances</span></span>

<span data-ttu-id="7e0e6-150">Indique qu’une instance de contient des valeurs fournies par les fournisseurs de propriétés dynamiques.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="7e0e6-151">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-151">The default is **TRUE**.</span></span>

<span data-ttu-id="7e0e6-152">Vous devez spécifier ce qualificateur sur une telle instance.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="7e0e6-153">Seule la valeur **true** est autorisée.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Des**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-155">Type de données **: \_ valeur booléenne CIM**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="7e0e6-156">S’applique à : instances</span><span class="sxs-lookup"><span data-stu-id="7e0e6-156">Applies to: instances</span></span>

<span data-ttu-id="7e0e6-157">Indique que la valeur de cette propriété ne peut pas changer pendant la durée de vie de l’instance.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-158"><span id="ID"></span><span id="id"></span>**IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-159">Type de données : **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="7e0e6-160">S’applique à : propriétés, paramètres</span><span class="sxs-lookup"><span data-stu-id="7e0e6-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="7e0e6-161">Identifie et séquence de manière unique une propriété ou un paramètre de méthode lorsque les instructions MOF sont générées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="7e0e6-162">Ce qualificateur est requis uniquement pour les paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="7e0e6-163">Lors de la création de paramètres pour une méthode, les concepteurs de classes doivent commencer par ID (0) pour le premier paramètre et utiliser chaque entier successif pour chaque paramètre successif.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="7e0e6-164">Si les qualificateurs d' **ID** ne sont pas intentionnellement omis, le compilateur MOF génère automatiquement des qualificateurs d' **ID** .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Été**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-166">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-166">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-167">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-167">Applies to: methods</span></span>

<span data-ttu-id="7e0e6-168">Indique qu’une méthode a une implémentation fournie par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-170">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-171">S’applique à : instances</span><span class="sxs-lookup"><span data-stu-id="7e0e6-171">Applies to: instances</span></span>

<span data-ttu-id="7e0e6-172">Indique qu’une instance de contient des valeurs fournies par un fournisseur de propriétés dynamiques.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="7e0e6-173">La valeur est passée au fournisseur de propriétés en tant qu’argument de la méthode [**IWbemPropertyProvider :: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-175">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-176">S’applique à : classes ou instances</span><span class="sxs-lookup"><span data-stu-id="7e0e6-176">Applies to: classes or instances</span></span>

<span data-ttu-id="7e0e6-177">Spécifie la langue d’origine pour une classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="7e0e6-178">Pour plus d’informations sur les valeurs de paramètres régionaux, consultez [codes de paramètres régionaux](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-180">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-180">Data type: **string array**</span></span>

<span data-ttu-id="7e0e6-181">S’applique à : instances d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e0e6-181">Applies to: namespace instances</span></span>

<span data-ttu-id="7e0e6-182">Spécifie un descripteur de sécurité pour l’espace de noms au format [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="7e0e6-183">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="7e0e6-184">La chaîne SDDL est traitée par WMI pour établir la sécurité de l’espace de noms, mais elle n’est pas stockée sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="7e0e6-185">Si aucun descripteur de sécurité n’est spécifié, la sécurité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="7e0e6-186">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-188">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-188">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-189">S’applique à : paramètres</span><span class="sxs-lookup"><span data-stu-id="7e0e6-189">Applies to: parameters</span></span>

<span data-ttu-id="7e0e6-190">Indique qu’un paramètre n’est pas obligatoire et qu’il a une valeur par défaut avec un comportement correct.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Autorisations**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-192">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-192">Data type: **string array**</span></span>

<span data-ttu-id="7e0e6-193">S’applique à : propriétés, méthodes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-193">Applies to: properties, methods</span></span>

<span data-ttu-id="7e0e6-194">Ensemble de valeurs utilisées pour informer le client des privilèges requis pour créer des instances, remplir des propriétés ou exécuter des méthodes.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="7e0e6-195">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-197">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-198">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="7e0e6-198">Applies to: properties</span></span>

<span data-ttu-id="7e0e6-199">Indique qu’une propriété d’instance contient des valeurs fournies par les fournisseurs de propriétés dynamiques.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="7e0e6-200">Vous devez spécifier ce qualificateur sur une telle propriété.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="7e0e6-201">La valeur est passée au fournisseur de propriétés en tant qu’argument de [**IWbemPropertyProvider :: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-203">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-204">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-204">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-205">La valeur de ce qualificateur est le nom du fournisseur dynamique qui fournit des instances de classe et actualise les données d’instance.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="7e0e6-206">Ce nom doit être inscrit auprès de WMI en créant une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) avec la propriété **Name** contenant ce nom.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="7e0e6-207">Quand ce qualificateur est spécifié sur une classe dont les instances sont fournies dynamiquement, le qualificateur **dynamique** doit également être spécifié.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-209">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-209">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-210">S’applique à : instances d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e0e6-210">Applies to: namespace instances</span></span>

<span data-ttu-id="7e0e6-211">Si la valeur est **true**, **RequiresEncryption** marque un espace de noms afin que les applications et les scripts clients doivent se connecter avec l’authentification chiffrée.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="7e0e6-212">Le niveau d’authentification doit être défini sur la **\_ \_ \_ \_ \_ confidentialité du niveau Authn C RPC** en C++.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="7e0e6-213">Dans les scripts ou les Visual Basic, le niveau d’authentification doit être défini sur **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="7e0e6-214">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="7e0e6-215">Le qualificateur est utilisé dans [*MOF*](gloss-m.md) avec la commande de préprocesseur d’espace de noms pragma.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="7e0e6-216">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md) ou [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="7e0e6-217">Les niveaux d’authentification de script sont définis dans [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="7e0e6-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-219">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-220">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-220">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-221">Désigne une classe qui ne peut avoir qu’une seule instance et qui ne contient pas de propriétés de clé.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="7e0e6-222">Seule la valeur **true** (valeur par défaut) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Statique**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-224">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-224">Data type: **boolean**</span></span>

<span data-ttu-id="7e0e6-225">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-225">Applies to: methods</span></span>

<span data-ttu-id="7e0e6-226">Indique si une méthode peut être appelée à l’aide de la définition de classe ou de ses instances.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="7e0e6-227">La méthode ne peut pas être appelée à partir d’une instance.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-229">Type de données : **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="7e0e6-230">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="7e0e6-230">Applies to: properties</span></span>

<span data-ttu-id="7e0e6-231">Indique qu’une propriété de type **\_ DateTime CIM** représente un intervalle de temps plutôt qu’une heure spécifique.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="7e0e6-232">Pour identifier la propriété en tant qu’intervalle, la valeur de ce qualificateur doit être « Interval ».</span><span class="sxs-lookup"><span data-stu-id="7e0e6-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="7e0e6-233">Toutes les autres valeurs de ce qualificateur sont réservées pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-234"><span id="UUID"></span><span id="uuid"></span>**UNIVERSEL**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-235">Data type: **string**</span></span>

<span data-ttu-id="7e0e6-236">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-236">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-237">Identificateur unique universel appliqué à la classe.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-239">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-239">Data type: **string**</span></span>

<span data-ttu-id="7e0e6-240">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-240">Applies to: classes</span></span>

<span data-ttu-id="7e0e6-241">Numéro de version de l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-241">The version number of the class object.</span></span> <span data-ttu-id="7e0e6-242">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-242">The default is **NULL**.</span></span> <span data-ttu-id="7e0e6-243">Le numéro de version est incrémenté lorsque des modifications sont apportées à la classe.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="7e0e6-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="7e0e6-245">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="7e0e6-245">Data type: **string array**</span></span>

<span data-ttu-id="7e0e6-246">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="7e0e6-246">Applies to: properties</span></span>

<span data-ttu-id="7e0e6-247">Ensemble de valeurs indiquant les privilèges système qui doivent être disponibles et activés pour une opération d’écriture réussie.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e0e6-248">Notes</span><span class="sxs-lookup"><span data-stu-id="7e0e6-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="7e0e6-249">Codes de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="7e0e6-249">Locale Codes</span></span>

<span data-ttu-id="7e0e6-250">Un code de paramètres régionaux se présente sous la forme « MS \_ <Three Digit Language ID> ».</span><span class="sxs-lookup"><span data-stu-id="7e0e6-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="7e0e6-251">Par exemple, les paramètres régionaux anglais sont MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="7e0e6-252">Le tableau suivant répertorie les ID de langue.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="7e0e6-253">Language</span><span class="sxs-lookup"><span data-stu-id="7e0e6-253">Language</span></span>              | <span data-ttu-id="7e0e6-254">ID de langue (hexadécimal)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="7e0e6-255">Arabe</span><span class="sxs-lookup"><span data-stu-id="7e0e6-255">Arabic</span></span>                | <span data-ttu-id="7e0e6-256">401</span><span class="sxs-lookup"><span data-stu-id="7e0e6-256">401</span></span>                       |
| <span data-ttu-id="7e0e6-257">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="7e0e6-258">416</span><span class="sxs-lookup"><span data-stu-id="7e0e6-258">416</span></span>                       |
| <span data-ttu-id="7e0e6-259">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="7e0e6-260">804</span><span class="sxs-lookup"><span data-stu-id="7e0e6-260">804</span></span>                       |
| <span data-ttu-id="7e0e6-261">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-261">Chinese (Traditional)</span></span> | <span data-ttu-id="7e0e6-262">404</span><span class="sxs-lookup"><span data-stu-id="7e0e6-262">404</span></span>                       |
| <span data-ttu-id="7e0e6-263">Tchèque</span><span class="sxs-lookup"><span data-stu-id="7e0e6-263">Czech</span></span>                 | <span data-ttu-id="7e0e6-264">405</span><span class="sxs-lookup"><span data-stu-id="7e0e6-264">405</span></span>                       |
| <span data-ttu-id="7e0e6-265">Danois</span><span class="sxs-lookup"><span data-stu-id="7e0e6-265">Danish</span></span>                | <span data-ttu-id="7e0e6-266">406</span><span class="sxs-lookup"><span data-stu-id="7e0e6-266">406</span></span>                       |
| <span data-ttu-id="7e0e6-267">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="7e0e6-267">Dutch</span></span>                 | <span data-ttu-id="7e0e6-268">413</span><span class="sxs-lookup"><span data-stu-id="7e0e6-268">413</span></span>                       |
| <span data-ttu-id="7e0e6-269">Anglais (par défaut)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-269">English (default)</span></span>     | <span data-ttu-id="7e0e6-270">409</span><span class="sxs-lookup"><span data-stu-id="7e0e6-270">409</span></span>                       |
| <span data-ttu-id="7e0e6-271">Finnois</span><span class="sxs-lookup"><span data-stu-id="7e0e6-271">Finnish</span></span>               | <span data-ttu-id="7e0e6-272">40b</span><span class="sxs-lookup"><span data-stu-id="7e0e6-272">40b</span></span>                       |
| <span data-ttu-id="7e0e6-273">Français</span><span class="sxs-lookup"><span data-stu-id="7e0e6-273">French</span></span>                | <span data-ttu-id="7e0e6-274">40c</span><span class="sxs-lookup"><span data-stu-id="7e0e6-274">40c</span></span>                       |
| <span data-ttu-id="7e0e6-275">Allemand</span><span class="sxs-lookup"><span data-stu-id="7e0e6-275">German</span></span>                | <span data-ttu-id="7e0e6-276">407</span><span class="sxs-lookup"><span data-stu-id="7e0e6-276">407</span></span>                       |
| <span data-ttu-id="7e0e6-277">Grec</span><span class="sxs-lookup"><span data-stu-id="7e0e6-277">Greek</span></span>                 | <span data-ttu-id="7e0e6-278">408</span><span class="sxs-lookup"><span data-stu-id="7e0e6-278">408</span></span>                       |
| <span data-ttu-id="7e0e6-279">Hébreu</span><span class="sxs-lookup"><span data-stu-id="7e0e6-279">Hebrew</span></span>                | <span data-ttu-id="7e0e6-280">40d</span><span class="sxs-lookup"><span data-stu-id="7e0e6-280">40d</span></span>                       |
| <span data-ttu-id="7e0e6-281">Hongrois</span><span class="sxs-lookup"><span data-stu-id="7e0e6-281">Hungarian</span></span>             | <span data-ttu-id="7e0e6-282">40e</span><span class="sxs-lookup"><span data-stu-id="7e0e6-282">40e</span></span>                       |
| <span data-ttu-id="7e0e6-283">Italien</span><span class="sxs-lookup"><span data-stu-id="7e0e6-283">Italian</span></span>               | <span data-ttu-id="7e0e6-284">410</span><span class="sxs-lookup"><span data-stu-id="7e0e6-284">410</span></span>                       |
| <span data-ttu-id="7e0e6-285">Japonais</span><span class="sxs-lookup"><span data-stu-id="7e0e6-285">Japanese</span></span>              | <span data-ttu-id="7e0e6-286">411</span><span class="sxs-lookup"><span data-stu-id="7e0e6-286">411</span></span>                       |
| <span data-ttu-id="7e0e6-287">Coréen</span><span class="sxs-lookup"><span data-stu-id="7e0e6-287">Korean</span></span>                | <span data-ttu-id="7e0e6-288">412</span><span class="sxs-lookup"><span data-stu-id="7e0e6-288">412</span></span>                       |
| <span data-ttu-id="7e0e6-289">Norvégien</span><span class="sxs-lookup"><span data-stu-id="7e0e6-289">Norwegian</span></span>             | <span data-ttu-id="7e0e6-290">414</span><span class="sxs-lookup"><span data-stu-id="7e0e6-290">414</span></span>                       |
| <span data-ttu-id="7e0e6-291">Polonais</span><span class="sxs-lookup"><span data-stu-id="7e0e6-291">Polish</span></span>                | <span data-ttu-id="7e0e6-292">415</span><span class="sxs-lookup"><span data-stu-id="7e0e6-292">415</span></span>                       |
| <span data-ttu-id="7e0e6-293">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="7e0e6-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="7e0e6-294">816</span><span class="sxs-lookup"><span data-stu-id="7e0e6-294">816</span></span>                       |
| <span data-ttu-id="7e0e6-295">Russe</span><span class="sxs-lookup"><span data-stu-id="7e0e6-295">Russian</span></span>               | <span data-ttu-id="7e0e6-296">419</span><span class="sxs-lookup"><span data-stu-id="7e0e6-296">419</span></span>                       |
| <span data-ttu-id="7e0e6-297">Espagnol</span><span class="sxs-lookup"><span data-stu-id="7e0e6-297">Spanish</span></span>               | <span data-ttu-id="7e0e6-298">c0a</span><span class="sxs-lookup"><span data-stu-id="7e0e6-298">c0a</span></span>                       |
| <span data-ttu-id="7e0e6-299">Suédois</span><span class="sxs-lookup"><span data-stu-id="7e0e6-299">Swedish</span></span>               | <span data-ttu-id="7e0e6-300">41D</span><span class="sxs-lookup"><span data-stu-id="7e0e6-300">41D</span></span>                       |
| <span data-ttu-id="7e0e6-301">Turc</span><span class="sxs-lookup"><span data-stu-id="7e0e6-301">Turkish</span></span>               | <span data-ttu-id="7e0e6-302">41f</span><span class="sxs-lookup"><span data-stu-id="7e0e6-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="7e0e6-303">Utilisation du \_ qualificateur GetObject Bypass</span><span class="sxs-lookup"><span data-stu-id="7e0e6-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="7e0e6-304">L’utilisation du qualificateur **\_ GetObject de contournement** sur une méthode peut produire des résultats confuss.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="7e0e6-305">L’exemple suivant définit les classes **Shape** et **Circle** .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="7e0e6-306">Notez que la classe **Circle** est dérivée de la classe **Shape** .</span><span class="sxs-lookup"><span data-stu-id="7e0e6-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="7e0e6-307">L’appel suivant à **ExecMethod** utilise un objet **Circle** nommé « MyCircle » pour dessiner un cercle.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="7e0e6-308">Dans le scénario précédent, WMI appelle **GetObject**; Découvre que « Shape. Name = 'MyCircle' » est un **cercle**; et exécute l’implémentation de **Circle** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="7e0e6-309">Toutefois, si vous utilisez le **qualificateur \_ GetObject du contournement** sur **DrawIt**, WMI n’appelle pas **GetObject**, ne découvre pas que « Shape. Name = 'MyCircle' » est un **cercle** et exécute l’implémentation de **la forme** de **DrawIt** au lieu de l’implémentation de **Circle** de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="7e0e6-310">L’appel suivant à **ExecMethod** appelle toujours l’implémentation correcte de **DrawIt**.</span><span class="sxs-lookup"><span data-stu-id="7e0e6-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="7e0e6-311">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e0e6-311">Requirements</span></span>



| <span data-ttu-id="7e0e6-312">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e0e6-312">Requirement</span></span> | <span data-ttu-id="7e0e6-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e0e6-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7e0e6-314">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e0e6-314">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0e6-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e0e6-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7e0e6-316">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e0e6-316">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0e6-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e0e6-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e0e6-318">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e0e6-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0e6-319">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="7e0e6-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="7e0e6-320">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="7e0e6-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="7e0e6-321">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="7e0e6-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

