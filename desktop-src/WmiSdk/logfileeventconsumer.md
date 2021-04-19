---
description: La classe LogFileEventConsumer écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: LogFileEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518414"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="91ced-103">LogFileEventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="91ced-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="91ced-104">La classe **LogFileEventConsumer** écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis.</span><span class="sxs-lookup"><span data-stu-id="91ced-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="91ced-105">Les chaînes sont séparées par des séquences de fin de ligne.</span><span class="sxs-lookup"><span data-stu-id="91ced-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="91ced-106">Cette classe est l’un des consommateurs d’événements standard fournis par WMI.</span><span class="sxs-lookup"><span data-stu-id="91ced-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="91ced-107">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="91ced-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ced-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="91ced-109">Membres</span><span class="sxs-lookup"><span data-stu-id="91ced-109">Members</span></span>

<span data-ttu-id="91ced-110">La classe **LogFileEventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="91ced-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="91ced-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91ced-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91ced-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91ced-112">Properties</span></span>

<span data-ttu-id="91ced-113">La classe **LogFileEventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="91ced-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91ced-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="91ced-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-115">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="91ced-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="91ced-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-117">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre.</span><span class="sxs-lookup"><span data-stu-id="91ced-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="91ced-118">WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="91ced-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="91ced-119">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="91ced-120">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="91ced-121">**Nom du fichier**</span><span class="sxs-lookup"><span data-stu-id="91ced-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91ced-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-124">Nom d’un fichier qui comprend le chemin d’accès auquel les entrées du journal sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="91ced-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="91ced-125">Si le fichier n’existe pas, **LogFileEventConsumer** tente de le créer.</span><span class="sxs-lookup"><span data-stu-id="91ced-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="91ced-126">Le consommateur échoue lorsque le chemin d’accès n’existe pas, ou lorsque l’utilisateur qui crée le consommateur ne dispose pas des autorisations d’écriture pour le fichier ou le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="91ced-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-127">**IsUnicode**</span><span class="sxs-lookup"><span data-stu-id="91ced-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="91ced-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-130">Si la **valeur est true**, le fichier journal est un fichier texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="91ced-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="91ced-131">Si la **valeur est false**, le fichier journal est un fichier texte de code multioctet.</span><span class="sxs-lookup"><span data-stu-id="91ced-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="91ced-132">Si le fichier existe, cette propriété est ignorée et le paramètre de fichier actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="91ced-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="91ced-133">Par exemple, si **IsUnicode** a la **valeur false**, mais que le fichier existant est un fichier Unicode, Unicode est utilisé.</span><span class="sxs-lookup"><span data-stu-id="91ced-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="91ced-134">Si **IsUnicode** a la **valeur true**, mais que le fichier est du code multioctet, le code multioctet est utilisé.</span><span class="sxs-lookup"><span data-stu-id="91ced-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="91ced-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91ced-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-138">Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="91ced-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="91ced-139">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="91ced-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="91ced-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-141">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91ced-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-143">Taille maximale d’un fichier journal en octets.</span><span class="sxs-lookup"><span data-stu-id="91ced-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="91ced-144">Si le fichier primaire dépasse sa taille maximale, le contenu est déplacé vers un autre fichier et le fichier primaire est vidé.</span><span class="sxs-lookup"><span data-stu-id="91ced-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="91ced-145">La valeur 0 (zéro) signifie qu’il n’y a aucune limite de taille.</span><span class="sxs-lookup"><span data-stu-id="91ced-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="91ced-146">La valeur par défaut est 65 535 octets.</span><span class="sxs-lookup"><span data-stu-id="91ced-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="91ced-147">La taille du fichier est vérifiée avant une opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="91ced-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="91ced-148">Par conséquent, vous pouvez avoir un fichier légèrement plus grand que la limite de taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="91ced-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="91ced-149">L’opération d’écriture suivante l’intercepte et démarre un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="91ced-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="91ced-150">La liste suivante identifie la structure d’affectation de noms pour le fichier de sauvegarde :</span><span class="sxs-lookup"><span data-stu-id="91ced-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="91ced-151">Si le nom de fichier d’origine est 8,3, l’extension est remplacée par une chaîne au format « 001 », « 002 », et ainsi de suite, par le plus petit nombre plus grand que tous les nombres précédemment utilisés et choisis.</span><span class="sxs-lookup"><span data-stu-id="91ced-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="91ced-152">Si « 999 » est utilisé, le nombre choisi est le plus petit nombre inutilisé.</span><span class="sxs-lookup"><span data-stu-id="91ced-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="91ced-153">Si le nom de fichier d’origine n’est pas 8,3, une chaîne au format « 001 », « 002 », et ainsi de suite, est ajoutée au nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="91ced-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="91ced-154">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91ced-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91ced-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="91ced-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91ced-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-158">File d’attente maximale pour un consommateur spécifique, en octets.</span><span class="sxs-lookup"><span data-stu-id="91ced-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="91ced-159">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="91ced-160">**Nom**</span><span class="sxs-lookup"><span data-stu-id="91ced-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91ced-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91ced-163">Qualificateurs : [ **clé**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="91ced-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="91ced-164">Nom unique de ce consommateur.</span><span class="sxs-lookup"><span data-stu-id="91ced-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="91ced-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ced-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="91ced-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91ced-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="91ced-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91ced-168">[Modèle](using-standard-string-templates.md) de chaîne standard pour le texte d’une entrée de journal.</span><span class="sxs-lookup"><span data-stu-id="91ced-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91ced-169">Notes</span><span class="sxs-lookup"><span data-stu-id="91ced-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91ced-170">**LogFileEventConsumer** ne sécurise pas le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="91ced-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="91ced-171">Par conséquent, quand vous configurez le **LogFileEventConsumer**, il est important de spécifier un répertoire qui est sécurisé au niveau dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="91ced-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="91ced-172">La classe **LogFileEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="91ced-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="91ced-173">Exemples</span><span class="sxs-lookup"><span data-stu-id="91ced-173">Examples</span></span>

<span data-ttu-id="91ced-174">Pour obtenir un exemple d’utilisation de **LogFileEventConsumer** pour créer un consommateur, consultez [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="91ced-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91ced-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ced-175">Requirements</span></span>



| <span data-ttu-id="91ced-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ced-176">Requirement</span></span> | <span data-ttu-id="91ced-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ced-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91ced-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ced-178">Minimum supported client</span></span><br/> | <span data-ttu-id="91ced-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91ced-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91ced-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ced-180">Minimum supported server</span></span><br/> | <span data-ttu-id="91ced-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91ced-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91ced-182">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91ced-182">Namespace</span></span><br/>                | <span data-ttu-id="91ced-183">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="91ced-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="91ced-184">MOF</span><span class="sxs-lookup"><span data-stu-id="91ced-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91ced-185"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91ced-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="91ced-186">DLL</span><span class="sxs-lookup"><span data-stu-id="91ced-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ced-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ced-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ced-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ced-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ced-189">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="91ced-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="91ced-190">Écriture dans un fichier journal basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="91ced-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="91ced-191">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="91ced-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="91ced-192">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="91ced-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="91ced-193">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="91ced-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

