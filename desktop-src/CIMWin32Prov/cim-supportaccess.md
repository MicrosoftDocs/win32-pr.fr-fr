---
description: La \_ classe CIM SupportAccess définit comment obtenir de l’aide pour un produit.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Classe CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110755"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="2e611-103">\_Classe CIM SupportAccess</span><span class="sxs-lookup"><span data-stu-id="2e611-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="2e611-104">La classe **CIM \_ SupportAccess** définit comment obtenir de l’aide pour un produit.</span><span class="sxs-lookup"><span data-stu-id="2e611-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e611-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2e611-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e611-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e611-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e611-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2e611-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2e611-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2e611-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e611-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e611-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="2e611-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2e611-110">Members</span></span>

<span data-ttu-id="2e611-111">La classe **CIM \_ SupportAccess** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e611-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="2e611-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e611-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e611-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e611-113">Properties</span></span>

<span data-ttu-id="2e611-114">La classe **CIM \_ SupportAccess** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e611-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e611-115">**CommunicationInfo**</span><span class="sxs-lookup"><span data-stu-id="2e611-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e611-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e611-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e611-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e611-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e611-118">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,11 "," MIF. \|FRU DMTF \| 002,12 ")</span><span class="sxs-lookup"><span data-stu-id="2e611-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="2e611-119">Détails du mode de communication.</span><span class="sxs-lookup"><span data-stu-id="2e611-119">Details of the communication mode.</span></span> <span data-ttu-id="2e611-120">Par exemple, si la propriété **CommunicationMode** est « Phone », cette propriété spécifie le numéro de téléphone à appeler.</span><span class="sxs-lookup"><span data-stu-id="2e611-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="2e611-121">**CommunicationMode**</span><span class="sxs-lookup"><span data-stu-id="2e611-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e611-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e611-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e611-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e611-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e611-124">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,5»)</span><span class="sxs-lookup"><span data-stu-id="2e611-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2e611-125">Forme de communication à utiliser pour obtenir un support.</span><span class="sxs-lookup"><span data-stu-id="2e611-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e611-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2e611-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="2e611-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Téléphone** (2)</span><span class="sxs-lookup"><span data-stu-id="2e611-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="2e611-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Télécopie** (3)</span><span class="sxs-lookup"><span data-stu-id="2e611-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="2e611-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="2e611-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="2e611-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Service en ligne** (5)</span><span class="sxs-lookup"><span data-stu-id="2e611-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="2e611-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Page Web** (6)</span><span class="sxs-lookup"><span data-stu-id="2e611-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e611-132">Page web</span><span class="sxs-lookup"><span data-stu-id="2e611-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="2e611-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="2e611-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="2e611-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Courrier électronique** (8)</span><span class="sxs-lookup"><span data-stu-id="2e611-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2e611-135">E-mail</span><span class="sxs-lookup"><span data-stu-id="2e611-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e611-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="2e611-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e611-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e611-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e611-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e611-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e611-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="2e611-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2e611-140">Description textuelle du type de prise en charge fourni.</span><span class="sxs-lookup"><span data-stu-id="2e611-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="2e611-141">**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="2e611-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e611-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e611-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e611-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e611-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e611-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Support \| 001,2 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2e611-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2e611-145">La région géographique ou le dialecte de langage auquel cette ressource de support appartient.</span><span class="sxs-lookup"><span data-stu-id="2e611-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="2e611-146">**SupportAccessId**</span><span class="sxs-lookup"><span data-stu-id="2e611-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e611-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2e611-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e611-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2e611-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e611-149">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e611-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e611-150">Chaîne de forme libre arbitraire définie par le fournisseur du produit ou par l’organisation qui déploie le produit.</span><span class="sxs-lookup"><span data-stu-id="2e611-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="2e611-151">Dans la mesure où il s’agit d’une clé, cette propriété doit être unique dans toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2e611-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e611-152">Notes</span><span class="sxs-lookup"><span data-stu-id="2e611-152">Remarks</span></span>

<span data-ttu-id="2e611-153">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2e611-153">WMI does not implement this class.</span></span>

<span data-ttu-id="2e611-154">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e611-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e611-155">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2e611-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e611-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e611-156">Requirements</span></span>



| <span data-ttu-id="2e611-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e611-157">Requirement</span></span> | <span data-ttu-id="2e611-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e611-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e611-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e611-159">Minimum supported client</span></span><br/> | <span data-ttu-id="2e611-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e611-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e611-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e611-161">Minimum supported server</span></span><br/> | <span data-ttu-id="2e611-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e611-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e611-163">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e611-163">Namespace</span></span><br/>                | <span data-ttu-id="2e611-164">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2e611-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e611-165">MOF</span><span class="sxs-lookup"><span data-stu-id="2e611-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e611-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e611-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e611-167">DLL</span><span class="sxs-lookup"><span data-stu-id="2e611-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e611-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e611-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

