---
description: La classe SMTPEventConsumer envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: SMTPEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210554"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="a9261-103">SMTPEventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="a9261-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="a9261-104">La classe **SMTPEventConsumer** envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="a9261-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="a9261-105">Un serveur SMTP doit exister sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="a9261-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="a9261-106">La classe SMTPEventConsumer ne prend pas en charge les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="a9261-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="a9261-107">L’encodage du message électronique doit être US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="a9261-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="a9261-108">Cette classe est l’un des consommateurs d’événements standard fournis par WMI.</span><span class="sxs-lookup"><span data-stu-id="a9261-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="a9261-109">Pour obtenir un exemple d’utilisation de **SMTPEventConsumer** pour créer un consommateur, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="a9261-110">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="a9261-111">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a9261-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a9261-112">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a9261-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9261-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9261-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="a9261-114">Membres</span><span class="sxs-lookup"><span data-stu-id="a9261-114">Members</span></span>

<span data-ttu-id="a9261-115">La classe **SMTPEventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9261-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="a9261-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9261-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9261-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9261-117">Properties</span></span>

<span data-ttu-id="a9261-118">La classe **SMTPEventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9261-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9261-119">**BccLine**</span><span class="sxs-lookup"><span data-stu-id="a9261-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-122">Liste d’adresses, séparées par une virgule ou un point-virgule, au format d’un modèle de chaîne standard auquel le message est envoyé en tant que copie carbone invisible.</span><span class="sxs-lookup"><span data-stu-id="a9261-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="a9261-123">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a9261-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-124">**CcLine**</span><span class="sxs-lookup"><span data-stu-id="a9261-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-127">Liste d’adresses, séparées par une virgule ou un point-virgule, dans le format d’un modèle de chaîne standard auquel le message est envoyé sous la forme d’une copie carbone.</span><span class="sxs-lookup"><span data-stu-id="a9261-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="a9261-128">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a9261-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-129">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="a9261-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-130">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="a9261-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a9261-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-132">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre.</span><span class="sxs-lookup"><span data-stu-id="a9261-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="a9261-133">WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a9261-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="a9261-134">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="a9261-135">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9261-136">**FromLine**</span><span class="sxs-lookup"><span data-stu-id="a9261-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-139">À partir de la ligne d’un message électronique au format d’un modèle de chaîne standard.</span><span class="sxs-lookup"><span data-stu-id="a9261-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="a9261-140">Si la **valeur est null**, une ligne de est construite sous la forme « winmgmt@*MachineName*».</span><span class="sxs-lookup"><span data-stu-id="a9261-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="a9261-141">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="a9261-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-142">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="a9261-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9261-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-144">Tableau de champs d’en-tête insérés dans un message électronique sans interprétation.</span><span class="sxs-lookup"><span data-stu-id="a9261-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="a9261-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-148">Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="a9261-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="a9261-149">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9261-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="a9261-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9261-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-153">File d’attente maximale pour un consommateur spécifique, en octets.</span><span class="sxs-lookup"><span data-stu-id="a9261-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="a9261-154">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9261-155">**Message**</span><span class="sxs-lookup"><span data-stu-id="a9261-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-158">Modèle de chaîne standard qui contient le corps d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="a9261-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-159">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a9261-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9261-162">Qualificateurs : [ **clé**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="a9261-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="a9261-163">Identificateur unique pour le consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="a9261-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-164">**ReplyToLine**</span><span class="sxs-lookup"><span data-stu-id="a9261-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-167">Ligne de réponse d’un message électronique au format d’un modèle de chaîne standard.</span><span class="sxs-lookup"><span data-stu-id="a9261-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="a9261-168">Si la **valeur est null**, aucune ligne reply-to n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a9261-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="a9261-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-172">Nom du serveur SMTP par le biais duquel un courrier électronique est envoyé.</span><span class="sxs-lookup"><span data-stu-id="a9261-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="a9261-173">Les noms autorisés sont une adresse IP ou un nom DNS ou NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="a9261-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="a9261-174">Cette propriété ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="a9261-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a9261-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-178">Modèle de chaîne standard qui contient l’objet d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="a9261-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="a9261-179">**ToLine**</span><span class="sxs-lookup"><span data-stu-id="a9261-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9261-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9261-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9261-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9261-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9261-182">Liste d’adresses, séparées par une virgule ou un point-virgule, dans le format d’un modèle de chaîne standard qui identifie l’emplacement où le message doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="a9261-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="a9261-183">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a9261-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9261-184">Notes</span><span class="sxs-lookup"><span data-stu-id="a9261-184">Remarks</span></span>

<span data-ttu-id="a9261-185">La classe SMTPEventConsumer est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="a9261-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="a9261-186">Certaines propriétés **ToLine**, **CcLine** ou **BccLine** peuvent avoir la **valeur null**, mais elles ne peuvent pas toutes avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a9261-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="a9261-187">La réception d’un code de retour d’erreur à partir du service SMTP est considérée comme un échec.</span><span class="sxs-lookup"><span data-stu-id="a9261-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="a9261-188">Exemples</span><span class="sxs-lookup"><span data-stu-id="a9261-188">Examples</span></span>

<span data-ttu-id="a9261-189">Pour obtenir un exemple d’utilisation de **SMTPEventConsumer** pour créer un consommateur, consultez [envoi de courriers électroniques en fonction d’un événement](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="a9261-190">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9261-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9261-191">Requirements</span></span>



| <span data-ttu-id="a9261-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9261-192">Requirement</span></span> | <span data-ttu-id="a9261-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9261-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9261-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9261-194">Minimum supported client</span></span><br/> | <span data-ttu-id="a9261-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9261-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9261-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9261-196">Minimum supported server</span></span><br/> | <span data-ttu-id="a9261-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9261-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9261-198">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9261-198">Namespace</span></span><br/>                | <span data-ttu-id="a9261-199">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="a9261-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="a9261-200">MOF</span><span class="sxs-lookup"><span data-stu-id="a9261-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9261-201"><dt>Smtpcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9261-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9261-202">DLL</span><span class="sxs-lookup"><span data-stu-id="a9261-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9261-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9261-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9261-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9261-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9261-205">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a9261-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="a9261-206">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="a9261-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="a9261-207">Envoi de courrier électronique à partir d’un événement</span><span class="sxs-lookup"><span data-stu-id="a9261-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="a9261-208">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="a9261-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="a9261-209">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="a9261-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




