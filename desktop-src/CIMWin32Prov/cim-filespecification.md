---
description: La \_ classe CIM FileSpecification représente un fichier qui se trouve sur le système ou en est déconnectée.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: Classe CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515565"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="abcda-103">\_Classe CIM FileSpecification</span><span class="sxs-lookup"><span data-stu-id="abcda-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="abcda-104">La classe **CIM \_ FileSpecification** représente un fichier qui se trouve sur le système ou en est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="abcda-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="abcda-105">Le fichier se trouve dans le répertoire identifié par l’Association [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="abcda-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="abcda-106">La méthode [**Invoke**](invoke-method-in-class-cim-filespecification.md) utilise les informations pour vérifier l’existence du fichier.</span><span class="sxs-lookup"><span data-stu-id="abcda-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="abcda-107">Notez que les propriétés avec une valeur **null** ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="abcda-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abcda-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="abcda-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="abcda-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="abcda-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="abcda-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="abcda-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="abcda-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="abcda-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="abcda-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abcda-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="abcda-113">Membres</span><span class="sxs-lookup"><span data-stu-id="abcda-113">Members</span></span>

<span data-ttu-id="abcda-114">La classe **CIM \_ FileSpecification** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="abcda-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="abcda-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abcda-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="abcda-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abcda-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="abcda-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abcda-117">Methods</span></span>

<span data-ttu-id="abcda-118">La classe **CIM \_ FileSpecification** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="abcda-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="abcda-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="abcda-119">Method</span></span>                                                         | <span data-ttu-id="abcda-120">Description</span><span class="sxs-lookup"><span data-stu-id="abcda-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="abcda-121">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="abcda-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="abcda-122">Évalue une vérification particulière.</span><span class="sxs-lookup"><span data-stu-id="abcda-122">Evaluates a particular check.</span></span> <span data-ttu-id="abcda-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="abcda-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="abcda-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abcda-124">Properties</span></span>

<span data-ttu-id="abcda-125">La classe **CIM \_ FileSpecification** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="abcda-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abcda-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="abcda-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="abcda-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-130">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="abcda-130">A short textual description of the subject.</span></span>

<span data-ttu-id="abcda-131">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="abcda-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-135">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="abcda-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-136">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="abcda-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="abcda-137">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="abcda-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="abcda-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abcda-141">Si la **valeur est true**, la condition est supposée exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="abcda-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="abcda-142">Par exemple, un fichier est censé se trouver sur un système. la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit donc retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="abcda-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="abcda-143">Si la **valeur est false**, la condition n’est pas censée exister.</span><span class="sxs-lookup"><span data-stu-id="abcda-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="abcda-144">Par exemple, un fichier ne se trouve pas sur un système, donc la méthode [**Invoke**](invoke-method-in-class-cim-check.md) doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="abcda-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="abcda-145">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-146">**EEPROM**</span><span class="sxs-lookup"><span data-stu-id="abcda-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abcda-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-149">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Signature du logiciel DMTF \| 002,4»)</span><span class="sxs-lookup"><span data-stu-id="abcda-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-150">Valeur calculée en tant que somme de 16 bits des 32 premiers octets du fichier.</span><span class="sxs-lookup"><span data-stu-id="abcda-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="abcda-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abcda-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-154">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Signature du logiciel DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="abcda-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-155">Valeur CRC calculée à l’aide du milieu 512 Ko.</span><span class="sxs-lookup"><span data-stu-id="abcda-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="abcda-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abcda-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-159">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Signature du logiciel DMTF \| 002,6»)</span><span class="sxs-lookup"><span data-stu-id="abcda-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-160">Valeur CRC pour le milieu 512 Ko du fichier, Modulo 3.</span><span class="sxs-lookup"><span data-stu-id="abcda-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-161">**CreateTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="abcda-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="abcda-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-164">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="abcda-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-165">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="abcda-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-166">**Description**</span><span class="sxs-lookup"><span data-stu-id="abcda-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abcda-169">Description des objets.</span><span class="sxs-lookup"><span data-stu-id="abcda-169">A description of the objects.</span></span>

<span data-ttu-id="abcda-170">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-171">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="abcda-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-172">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abcda-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-174">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="abcda-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-175">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="abcda-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="abcda-176">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="abcda-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="abcda-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-180">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="abcda-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-181">Algorithme permettant de calculer une somme de contrôle 128 bits pour tout fichier ou objet.</span><span class="sxs-lookup"><span data-stu-id="abcda-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="abcda-182">La probabilité que deux fichiers différents produisent la même somme de contrôle MD5 est très petite (environ 1 dans 2 ^ 64) et la somme de contrôle MD5 d’un fichier peut être utilisée pour construire un identificateur de contenu fiable susceptible d’identifier le fichier de façon unique.</span><span class="sxs-lookup"><span data-stu-id="abcda-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="abcda-183">L’inverse est également vrai.</span><span class="sxs-lookup"><span data-stu-id="abcda-183">The reverse is also true.</span></span> <span data-ttu-id="abcda-184">Si deux fichiers ont la même somme de contrôle MD5, il est très probable que les fichiers soient identiques.</span><span class="sxs-lookup"><span data-stu-id="abcda-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="abcda-185">À des fins de spécification MOF de la propriété MD5, l’algorithme MD5 génère toujours une chaîne de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="abcda-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="abcda-186">Par exemple, la chaîne « abcdefghijklmnopqrstuvwxyz » génère la chaîne « c3fcd3d76192e4007dfb496cca67e13b ».</span><span class="sxs-lookup"><span data-stu-id="abcda-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="abcda-187">Pour plus d’informations sur l’implémentation de l’algorithme MD5, consultez [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="abcda-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-188">**Nom**</span><span class="sxs-lookup"><span data-stu-id="abcda-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-191">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="abcda-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-192">Soit le nom du fichier, soit le nom du fichier avec un préfixe de répertoire.</span><span class="sxs-lookup"><span data-stu-id="abcda-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="abcda-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-196">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="abcda-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-197">Il s’agit d’un identificateur pour cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="abcda-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="abcda-198">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="abcda-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="abcda-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-200">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abcda-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-202">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="abcda-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="abcda-203">État de l’élément logiciel d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="abcda-203">The software element state of a software element.</span></span>

<span data-ttu-id="abcda-204">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="abcda-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="abcda-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-206">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="abcda-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="abcda-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="abcda-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-208">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="abcda-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="abcda-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="abcda-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-210">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="abcda-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="abcda-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="abcda-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-212">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="abcda-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="abcda-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="abcda-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-214">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abcda-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-216">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="abcda-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-217">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="abcda-217">Target operating system of the software element.</span></span>

<span data-ttu-id="abcda-218">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abcda-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="abcda-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abcda-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="abcda-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="abcda-221"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="abcda-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="abcda-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="abcda-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="abcda-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-224">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="abcda-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="abcda-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="abcda-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="abcda-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="abcda-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="abcda-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="abcda-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="abcda-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="abcda-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-229">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="abcda-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="abcda-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="abcda-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="abcda-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="abcda-232"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="abcda-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="abcda-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="abcda-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="abcda-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="abcda-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="abcda-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="abcda-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="abcda-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="abcda-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-237">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="abcda-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="abcda-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="abcda-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="abcda-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="abcda-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="abcda-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="abcda-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="abcda-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="abcda-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="abcda-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="abcda-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="abcda-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="abcda-245"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="abcda-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="abcda-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="abcda-247"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="abcda-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="abcda-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="abcda-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="abcda-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="abcda-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="abcda-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="abcda-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="abcda-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="abcda-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="abcda-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="abcda-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="abcda-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="abcda-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="abcda-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="abcda-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="abcda-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="abcda-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="abcda-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="abcda-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="abcda-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="abcda-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="abcda-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="abcda-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="abcda-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="abcda-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="abcda-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="abcda-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="abcda-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="abcda-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-263">Une série</span><span class="sxs-lookup"><span data-stu-id="abcda-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="abcda-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="abcda-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-265">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="abcda-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="abcda-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="abcda-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-267">NT tandem</span><span class="sxs-lookup"><span data-stu-id="abcda-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="abcda-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="abcda-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="abcda-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="abcda-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="abcda-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="abcda-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="abcda-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="abcda-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="abcda-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="abcda-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="abcda-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="abcda-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="abcda-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="abcda-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="abcda-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-276">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="abcda-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="abcda-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="abcda-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="abcda-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="abcda-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="abcda-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="abcda-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="abcda-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="abcda-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="abcda-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="abcda-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="abcda-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="abcda-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="abcda-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="abcda-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="abcda-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="abcda-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="abcda-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="abcda-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="abcda-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="abcda-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="abcda-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="abcda-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="abcda-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="abcda-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="abcda-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="abcda-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="abcda-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="abcda-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="abcda-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="abcda-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="abcda-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="abcda-293">Palm OS</span><span class="sxs-lookup"><span data-stu-id="abcda-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="abcda-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="abcda-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="abcda-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="abcda-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="abcda-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="abcda-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="abcda-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="abcda-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="abcda-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="abcda-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abcda-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="abcda-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="abcda-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abcda-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-302">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="abcda-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-303">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="abcda-303">Version of the operation.</span></span>

<span data-ttu-id="abcda-304">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="abcda-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="abcda-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="abcda-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="abcda-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="abcda-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="abcda-307">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abcda-308">Notes</span><span class="sxs-lookup"><span data-stu-id="abcda-308">Remarks</span></span>

<span data-ttu-id="abcda-309">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="abcda-309">WMI does not implement this class.</span></span> <span data-ttu-id="abcda-310">Pour les classes dérivées de **CIM \_ FileSpecification**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="abcda-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="abcda-311">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="abcda-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="abcda-312">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="abcda-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="abcda-313">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abcda-313">Requirements</span></span>



| <span data-ttu-id="abcda-314">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abcda-314">Requirement</span></span> | <span data-ttu-id="abcda-315">Valeur</span><span class="sxs-lookup"><span data-stu-id="abcda-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abcda-316">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abcda-316">Minimum supported client</span></span><br/> | <span data-ttu-id="abcda-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abcda-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abcda-318">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abcda-318">Minimum supported server</span></span><br/> | <span data-ttu-id="abcda-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abcda-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abcda-320">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="abcda-320">Namespace</span></span><br/>                | <span data-ttu-id="abcda-321">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="abcda-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abcda-322">MOF</span><span class="sxs-lookup"><span data-stu-id="abcda-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abcda-323"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abcda-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abcda-324">DLL</span><span class="sxs-lookup"><span data-stu-id="abcda-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abcda-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abcda-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abcda-326">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abcda-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcda-327">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="abcda-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

