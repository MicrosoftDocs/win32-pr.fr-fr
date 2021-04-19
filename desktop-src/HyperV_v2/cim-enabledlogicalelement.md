---
description: Représente un élément logique qui peut être activé et désactivé.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: Classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527509"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="14a66-103">\_Classe CIM EnabledLogicalElement</span><span class="sxs-lookup"><span data-stu-id="14a66-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="14a66-104">Représente un élément logique qui peut être activé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="14a66-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14a66-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="14a66-106">Membres</span><span class="sxs-lookup"><span data-stu-id="14a66-106">Members</span></span>

<span data-ttu-id="14a66-107">La classe **CIM \_ EnabledLogicalElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14a66-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="14a66-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14a66-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="14a66-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14a66-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14a66-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14a66-110">Methods</span></span>

<span data-ttu-id="14a66-111">La classe **CIM \_ EnabledLogicalElement** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="14a66-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="14a66-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="14a66-112">Method</span></span>                                                                     | <span data-ttu-id="14a66-113">Description</span><span class="sxs-lookup"><span data-stu-id="14a66-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="14a66-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="14a66-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="14a66-115">Demande que l’état de l’élément soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="14a66-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="14a66-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14a66-116">Properties</span></span>

<span data-ttu-id="14a66-117">La classe **CIM \_ EnabledLogicalElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="14a66-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14a66-118">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="14a66-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-119">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a66-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a66-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a66-121">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span><span class="sxs-lookup"><span data-stu-id="14a66-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="14a66-122">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="14a66-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="14a66-123">Les valeurs répertoriées doivent être un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l' **instance \_ EnabledLogicalElementCapabilities CIM** associée.</span><span class="sxs-lookup"><span data-stu-id="14a66-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="14a66-124">Cette propriété a la **valeur null** si l’implémentation ne peut pas déterminer le jeu de valeurs possibles pour l’état actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="14a66-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14a66-125">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="14a66-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14a66-126">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="14a66-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="14a66-127">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="14a66-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="14a66-128">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="14a66-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="14a66-129">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="14a66-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="14a66-130">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="14a66-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="14a66-131">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="14a66-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="14a66-132">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="14a66-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="14a66-133">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="14a66-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14a66-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14a66-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14a66-135">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="14a66-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-136">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a66-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="14a66-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14a66-138">Indique la configuration de démarrage ou par défaut d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="14a66-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="14a66-139">Valeur par défaut **activée** (2).</span><span class="sxs-lookup"><span data-stu-id="14a66-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14a66-140">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="14a66-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14a66-141">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="14a66-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14a66-142">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="14a66-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="14a66-143">**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="14a66-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="14a66-144">**Pas de valeur par défaut** (7)</span><span class="sxs-lookup"><span data-stu-id="14a66-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="14a66-145">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="14a66-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14a66-146">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14a66-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="14a66-147">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14a66-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14a66-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="14a66-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a66-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a66-151">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**OtherEnabledState**")</span><span class="sxs-lookup"><span data-stu-id="14a66-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="14a66-152">Indique l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="14a66-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="14a66-153">Les valeurs possibles incluent les transitions entre les États.</span><span class="sxs-lookup"><span data-stu-id="14a66-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="14a66-154">Par exemple, **l’arrêt** (4) et le **démarrage** de (10) sont des États transitoires entre **activé** et **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="14a66-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14a66-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14a66-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14a66-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="14a66-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14a66-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="14a66-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-158">L’élément est ou peut exécuter des commandes, traite toutes les commandes mises en file d’attente et met en file d’attente les nouvelles requêtes.</span><span class="sxs-lookup"><span data-stu-id="14a66-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14a66-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="14a66-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-160">l’élément n’exécutera pas de commande et supprimera toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="14a66-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="14a66-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="14a66-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-162">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="14a66-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14a66-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="14a66-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-164">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="14a66-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="14a66-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="14a66-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-166">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="14a66-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="14a66-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans test** (7)</span><span class="sxs-lookup"><span data-stu-id="14a66-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-168">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="14a66-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="14a66-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="14a66-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-170">L’élément peut exécuter des commandes, mais met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="14a66-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="14a66-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="14a66-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-172">Que l’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="14a66-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="14a66-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (10)</span><span class="sxs-lookup"><span data-stu-id="14a66-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-174">L’élément est en train d’accéder à un état activé.</span><span class="sxs-lookup"><span data-stu-id="14a66-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="14a66-175">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="14a66-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14a66-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="14a66-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="14a66-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14a66-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14a66-178">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="14a66-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="14a66-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a66-181">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="14a66-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="14a66-182">Décrit l’état de l’élément lorsque la valeur de la propriété **EnabledState** est **other**.</span><span class="sxs-lookup"><span data-stu-id="14a66-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="14a66-183">Cette propriété doit être définie sur **null** lorsque **EnabledState** n’est pas **autre**.</span><span class="sxs-lookup"><span data-stu-id="14a66-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="14a66-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="14a66-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a66-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a66-187">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="14a66-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="14a66-188">Indique le dernier État demandé pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="14a66-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="14a66-189">L’état actuel est indiqué par la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="14a66-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="14a66-190">Cette propriété vous permet de comparer les derniers États demandés et actuels.</span><span class="sxs-lookup"><span data-stu-id="14a66-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="14a66-191">Lorsque la valeur de la propriété **EnabledState** n’est **pas applicable**, cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="14a66-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14a66-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14a66-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-193">Le dernier État demandé pour l’élément est inconnu.</span><span class="sxs-lookup"><span data-stu-id="14a66-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14a66-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="14a66-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14a66-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="14a66-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-196">Demande une désactivation immédiate de l’élément, de sorte qu’il n’exécute pas ou n’accepte aucune commande ou traitement de requêtes.</span><span class="sxs-lookup"><span data-stu-id="14a66-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="14a66-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="14a66-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-198">Demande un passage ordonné à l’état désactivé et peut impliquer la suppression de la puissance, afin d’effacer complètement tout état existant.</span><span class="sxs-lookup"><span data-stu-id="14a66-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="14a66-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Aucune modification** (5)</span><span class="sxs-lookup"><span data-stu-id="14a66-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-200">Déconseillé au lieu d’indiquer que le dernier État demandé est « inconnu » (0).</span><span class="sxs-lookup"><span data-stu-id="14a66-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="14a66-201">Si le dernier État demandé ou souhaité est inconnu, **RequestedState** doit avoir la valeur « Unknown » (0), mais peut avoir la valeur « no change » (5).</span><span class="sxs-lookup"><span data-stu-id="14a66-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="14a66-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="14a66-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-203">L’élément a été demandé à la transition vers l' **EnabledState** activé mais hors connexion.</span><span class="sxs-lookup"><span data-stu-id="14a66-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="14a66-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="14a66-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="14a66-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="14a66-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="14a66-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="14a66-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="14a66-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="14a66-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-208">Fait référence à l’arrêt et au passage à un état « activé ».</span><span class="sxs-lookup"><span data-stu-id="14a66-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="14a66-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="14a66-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="14a66-210">Indique que l’élément est d’abord « désactivé », puis « activé ».</span><span class="sxs-lookup"><span data-stu-id="14a66-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14a66-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (12)</span><span class="sxs-lookup"><span data-stu-id="14a66-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14a66-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14a66-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="14a66-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14a66-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14a66-214">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="14a66-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-215">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14a66-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14a66-217">Indique l’état de la dernière modification de l’élément.</span><span class="sxs-lookup"><span data-stu-id="14a66-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="14a66-218">Si l’état de l’élément n’a pas changé et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="14a66-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="14a66-219">Si une modification d’État a été demandée, mais a été rejetée ou n’est pas encore traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="14a66-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="14a66-220">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="14a66-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a66-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14a66-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14a66-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="14a66-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a66-223">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","**CIM \_ EnabledLogicalElement**.**RequestedState**","**CIM \_ EnabledLogicalElement**.**EnabledState**»)</span><span class="sxs-lookup"><span data-stu-id="14a66-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="14a66-224">Indique l’État cible vers lequel l’instance change.</span><span class="sxs-lookup"><span data-stu-id="14a66-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="14a66-225">La valeur **no change** indique qu’aucune transition n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="14a66-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="14a66-226">La valeur **non applicable** indique que l’implémentation ne signale pas les transitions en cours.</span><span class="sxs-lookup"><span data-stu-id="14a66-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14a66-227">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="14a66-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14a66-228">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="14a66-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14a66-229">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="14a66-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="14a66-230">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="14a66-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="14a66-231">**Aucune modification** (5)</span><span class="sxs-lookup"><span data-stu-id="14a66-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="14a66-232">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="14a66-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="14a66-233">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="14a66-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="14a66-234">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="14a66-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="14a66-235">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="14a66-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="14a66-236">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="14a66-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="14a66-237">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="14a66-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14a66-238">**Non applicable** (12)</span><span class="sxs-lookup"><span data-stu-id="14a66-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="14a66-239">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="14a66-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="14a66-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="14a66-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="14a66-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14a66-241">Requirements</span></span>



| <span data-ttu-id="14a66-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14a66-242">Requirement</span></span> | <span data-ttu-id="14a66-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="14a66-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a66-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14a66-244">Minimum supported client</span></span><br/> | <span data-ttu-id="14a66-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14a66-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14a66-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14a66-246">Minimum supported server</span></span><br/> | <span data-ttu-id="14a66-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14a66-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14a66-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="14a66-248">Namespace</span></span><br/>                | <span data-ttu-id="14a66-249">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="14a66-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14a66-250">MOF</span><span class="sxs-lookup"><span data-stu-id="14a66-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14a66-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14a66-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14a66-252">DLL</span><span class="sxs-lookup"><span data-stu-id="14a66-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14a66-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14a66-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14a66-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14a66-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a66-255">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="14a66-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

