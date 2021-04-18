---
description: Représente l’en-tête commun utilisé par toutes les classes MSMCAEvent. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536538"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="984a8-104">\_Classe d’en-tête MSMCAEvent</span><span class="sxs-lookup"><span data-stu-id="984a8-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="984a8-105">La classe d' **\_ en-tête MSMCAEvent** représente l’en-tête commun utilisé par toutes les [classes MSMCA](msmca-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="984a8-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="984a8-106">Les fichiers d’en-tête sont utilisés afin que le code C et C++ puisse avoir une structure de données qui décrit l’en-tête commun pour tous les événements.</span><span class="sxs-lookup"><span data-stu-id="984a8-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="984a8-107">Cette classe est réservée à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="984a8-107">This class is reserved for internal use.</span></span> <span data-ttu-id="984a8-108">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="984a8-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="984a8-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="984a8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="984a8-110">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="984a8-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="984a8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="984a8-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="984a8-112">Membres</span><span class="sxs-lookup"><span data-stu-id="984a8-112">Members</span></span>

<span data-ttu-id="984a8-113">La classe d' **\_ en-tête MSMCAEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="984a8-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="984a8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="984a8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="984a8-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="984a8-115">Properties</span></span>

<span data-ttu-id="984a8-116">La classe d' **\_ en-tête MSMCAEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="984a8-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="984a8-117">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="984a8-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="984a8-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-120">Nombre d’erreurs supplémentaires dans l’enregistrement MCA.</span><span class="sxs-lookup"><span data-stu-id="984a8-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="984a8-121">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="984a8-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="984a8-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-124">UC qui signale l’erreur.</span><span class="sxs-lookup"><span data-stu-id="984a8-124">CPU that reports the error.</span></span> <span data-ttu-id="984a8-125">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="984a8-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="984a8-126">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="984a8-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-127">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="984a8-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-129">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="984a8-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="984a8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="984a8-130">Value</span></span>                                                                                                | <span data-ttu-id="984a8-131">Signification</span><span class="sxs-lookup"><span data-stu-id="984a8-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="984a8-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="984a8-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="984a8-133">Récupérable</span><span class="sxs-lookup"><span data-stu-id="984a8-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="984a8-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="984a8-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="984a8-135">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="984a8-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="984a8-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="984a8-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="984a8-137">Corrigible</span><span class="sxs-lookup"><span data-stu-id="984a8-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="984a8-138">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="984a8-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="984a8-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-141">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="984a8-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="984a8-142">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="984a8-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="984a8-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-145">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="984a8-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="984a8-146">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="984a8-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="984a8-147">**Type**</span><span class="sxs-lookup"><span data-stu-id="984a8-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984a8-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="984a8-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="984a8-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984a8-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984a8-150">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="984a8-150">Type of event log message.</span></span> <span data-ttu-id="984a8-151">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="984a8-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="984a8-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="984a8-152">Requirements</span></span>



| <span data-ttu-id="984a8-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="984a8-153">Requirement</span></span> | <span data-ttu-id="984a8-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="984a8-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="984a8-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984a8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="984a8-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="984a8-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="984a8-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984a8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="984a8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="984a8-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="984a8-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="984a8-159">Namespace</span></span><br/>                | <span data-ttu-id="984a8-160">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="984a8-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="984a8-161">MOF</span><span class="sxs-lookup"><span data-stu-id="984a8-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="984a8-162"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="984a8-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="984a8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="984a8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="984a8-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="984a8-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="984a8-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="984a8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984a8-166">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="984a8-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="984a8-167">Classes WMI C++</span><span class="sxs-lookup"><span data-stu-id="984a8-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

