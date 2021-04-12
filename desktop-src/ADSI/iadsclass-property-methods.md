---
title: Méthodes de propriété IADsClass (IADs. h)
description: Les méthodes de propriété de l’interface IADsClass obtiennent ou définissent les propriétés suivantes. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105154"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="d3e27-105">Méthodes de propriété IADsClass</span><span class="sxs-lookup"><span data-stu-id="d3e27-105">IADsClass Property Methods</span></span>

<span data-ttu-id="d3e27-106">Les méthodes de propriété de l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtiennent ou définissent les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3e27-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="d3e27-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d3e27-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d3e27-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3e27-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d3e27-109">**Résumé**</span><span class="sxs-lookup"><span data-stu-id="d3e27-109">**Abstract**</span></span>
<span data-ttu-id="d3e27-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-111">Valeur booléenne qui indique si cette classe est abstraite ou non abstraite.</span><span class="sxs-lookup"><span data-stu-id="d3e27-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="d3e27-112">Lorsque la **valeur est true**, cette classe est une classe abstraite qui ne peut pas être instanciée directement dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d3e27-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="d3e27-113">Les classes abstraites ne peuvent être utilisées qu’en tant que Super classes.</span><span class="sxs-lookup"><span data-stu-id="d3e27-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="d3e27-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-115">Type de données de script : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d3e27-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-116">**AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="d3e27-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="d3e27-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-118">Tableau de chaînes ADsPath qui indiquent les classes Super auxiliaires dont cette classe dérive.</span><span class="sxs-lookup"><span data-stu-id="d3e27-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="d3e27-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-120">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-121">**Appoint**</span><span class="sxs-lookup"><span data-stu-id="d3e27-121">**Auxiliary**</span></span>
<span data-ttu-id="d3e27-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-123">Valeur booléenne qui indique si cette classe est auxiliaire ou non.</span><span class="sxs-lookup"><span data-stu-id="d3e27-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="d3e27-124">Lorsque la **valeur est true**, cette classe est une classe auxiliaire et ne peut pas être instanciée directement dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d3e27-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="d3e27-125">Les classes auxiliaires ne peuvent être utilisées qu’en tant que Super classes d’autres classes auxiliaires ou en tant que source de propriétés supplémentaires sur les classes structurelles.</span><span class="sxs-lookup"><span data-stu-id="d3e27-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="d3e27-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-127">Type de données de script : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d3e27-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-128">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="d3e27-128">**CLSID**</span></span>
<span data-ttu-id="d3e27-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-130">CLSID spécifique au fournisseur facultatif identifiant l’objet COM qui implémente cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3e27-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="d3e27-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-132">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3e27-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-133">**Conteneur**</span><span class="sxs-lookup"><span data-stu-id="d3e27-133">**Container**</span></span>
<span data-ttu-id="d3e27-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-135">Valeur booléenne qui indique si cette classe peut être un conteneur d’autres classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="d3e27-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="d3e27-136">Si cette valeur est **true**, vous pouvez appeler la méthode d' **extraction de \_ conteneur** pour récupérer un tableau des classes d’objets que cette classe peut contenir.</span><span class="sxs-lookup"><span data-stu-id="d3e27-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="d3e27-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-138">Type de données de script : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d3e27-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-139">**Containment**</span><span class="sxs-lookup"><span data-stu-id="d3e27-139">**Containment**</span></span>
<span data-ttu-id="d3e27-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-141">Tableau **BSTR** dans lequel chaque élément est le nom d’une classe d’objet que cette classe peut contenir.</span><span class="sxs-lookup"><span data-stu-id="d3e27-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="d3e27-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-143">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-144">**DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="d3e27-144">**DerivedFrom**</span></span>
<span data-ttu-id="d3e27-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-146">Tableau de chaînes ADsPath qui indiquent les classes à partir desquelles cette classe a été dérivée.</span><span class="sxs-lookup"><span data-stu-id="d3e27-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="d3e27-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-148">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-149">**HelpFileContext**</span><span class="sxs-lookup"><span data-stu-id="d3e27-149">**HelpFileContext**</span></span>
<span data-ttu-id="d3e27-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-151">ID de contexte dans **HelpFileName** où se trouvent des informations spécifiques pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3e27-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="d3e27-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-153">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="d3e27-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-154">**HelpFileName**</span><span class="sxs-lookup"><span data-stu-id="d3e27-154">**HelpFileName**</span></span>
<span data-ttu-id="d3e27-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-156">Nom d’un fichier d’aide qui contient plus d’informations sur les objets de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3e27-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="d3e27-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-158">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3e27-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-159">**MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="d3e27-159">**MandatoryProperties**</span></span>
<span data-ttu-id="d3e27-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-161">**SAFEARRAY** de **Variant** s qui répertorie les propriétés qui doivent être définies pour que cette classe soit écrite dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="d3e27-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="d3e27-162">Si la classe ne contient qu’une seule propriété, l’opération **obtenir \_ MandatoryProperties** retourne un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="d3e27-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="d3e27-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-164">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-165">**NamingProperties**</span><span class="sxs-lookup"><span data-stu-id="d3e27-165">**NamingProperties**</span></span>
<span data-ttu-id="d3e27-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-167">**SAFEARRAY** de **BSTR** qui répertorie les propriétés utilisées pour nommer les attributs de cette classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="d3e27-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="d3e27-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-169">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-170">**OID**</span><span class="sxs-lookup"><span data-stu-id="d3e27-170">**OID**</span></span>
<span data-ttu-id="d3e27-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-172">Identificateur d’objet spécifique au fournisseur qui définit cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3e27-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="d3e27-173">Cela est fourni pour autoriser l’extension de schéma, à l’aide de Active Directory, dans les services d’annuaire qui requièrent des OID spécifiques au fournisseur pour les classes.</span><span class="sxs-lookup"><span data-stu-id="d3e27-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="d3e27-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-175">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3e27-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-176">**(OptionalProperties)**</span><span class="sxs-lookup"><span data-stu-id="d3e27-176">**OptionalProperties**</span></span>
<span data-ttu-id="d3e27-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-178">**SAFEARRAY** de **Variant** s qui répertorie les propriétés facultatives de cette classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="d3e27-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="d3e27-179">Si la classe ne contient qu’une seule propriété, l’opération **obtenir \_ (OptionalProperties)** retourne un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="d3e27-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="d3e27-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-181">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-182">**PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="d3e27-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="d3e27-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-184">Tableau de chaînes ADsPath qui indiquent les classes de schéma qui peuvent contenir des instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3e27-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="d3e27-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e27-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-186">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="d3e27-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e27-187">**PrimaryInterface**</span><span class="sxs-lookup"><span data-stu-id="d3e27-187">**PrimaryInterface**</span></span>
<span data-ttu-id="d3e27-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3e27-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3e27-189">GUID d’identificateur spécifique au fournisseur facultatif qui associe une interface aux objets de cette classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="d3e27-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="d3e27-190">Par exemple, la classe « User » qui prend en charge [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) et **PrimaryInterface** est identifiée par l' **IID \_ IADsUser**.</span><span class="sxs-lookup"><span data-stu-id="d3e27-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="d3e27-191">Ce doit être au format de chaîne standard d’un GUID, tel que défini par COM.</span><span class="sxs-lookup"><span data-stu-id="d3e27-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="d3e27-192">Ce GUID est la valeur qui apparaît dans la propriété [**IADs :: obtenir \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) dans les instances de cette classe pour les fournisseurs qui implémentent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d3e27-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="d3e27-193">L’identification d’une classe de schéma par l’IID de l’interface principale du code de la classe permet d’utiliser **QueryInterface** au moment de l’exécution pour déterminer si un objet est de la classe souhaitée.</span><span class="sxs-lookup"><span data-stu-id="d3e27-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="d3e27-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e27-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3e27-195">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3e27-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d3e27-196">Exemples</span><span class="sxs-lookup"><span data-stu-id="d3e27-196">Examples</span></span>

<span data-ttu-id="d3e27-197">L’exemple de code suivant montre comment utiliser l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) pour déterminer si un objet peut être un conteneur et, le cas échéant, répertorie les noms de tous les objets qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="d3e27-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="d3e27-198">L’exemple de code suivant montre comment utiliser l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) pour déterminer si un objet peut être un conteneur et, le cas échéant, répertorie les noms de tous les objets qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="d3e27-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="d3e27-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3e27-199">Requirements</span></span>



| <span data-ttu-id="d3e27-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3e27-200">Requirement</span></span> | <span data-ttu-id="d3e27-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3e27-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e27-202">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3e27-202">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e27-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3e27-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3e27-204">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3e27-204">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e27-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3e27-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3e27-206">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3e27-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e27-207"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e27-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d3e27-208">DLL</span><span class="sxs-lookup"><span data-stu-id="d3e27-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3e27-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3e27-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3e27-210">IID</span><span class="sxs-lookup"><span data-stu-id="d3e27-210">IID</span></span><br/>                      | <span data-ttu-id="d3e27-211">IID \_ IADsClass est défini en tant que C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="d3e27-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d3e27-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3e27-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e27-213">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="d3e27-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="d3e27-214">**IADsClass :: qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="d3e27-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





