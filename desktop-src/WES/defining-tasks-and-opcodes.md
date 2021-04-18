---
title: Définition des tâches et des OpCodes
description: Les fournisseurs utilisent des tâches et des OpCodes pour regrouper logiquement les événements. Le regroupement d’événements permet aux consommateurs de rechercher uniquement les événements qui contiennent des combinaisons tâche et opcode spécifiques.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507850"
---
# <a name="defining-tasks-and-opcodes"></a><span data-ttu-id="7f632-104">Définition des tâches et des OpCodes</span><span class="sxs-lookup"><span data-stu-id="7f632-104">Defining Tasks and Opcodes</span></span>

<span data-ttu-id="7f632-105">Les fournisseurs utilisent des tâches et des OpCodes pour regrouper logiquement les événements.</span><span class="sxs-lookup"><span data-stu-id="7f632-105">Providers use tasks and opcodes to logically group events.</span></span> <span data-ttu-id="7f632-106">Le regroupement d’événements permet aux consommateurs de rechercher uniquement les événements qui contiennent des combinaisons tâche et opcode spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7f632-106">Grouping events helps consumers query for only those events that contain specific task and opcode combinations.</span></span> <span data-ttu-id="7f632-107">En règle générale, vous utilisez des tâches pour identifier un composant majeur du fournisseur, tel que le réseau ou le composant de base de données.</span><span class="sxs-lookup"><span data-stu-id="7f632-107">Typically, you use tasks to identify a major component of the provider such as the networking or database component.</span></span> <span data-ttu-id="7f632-108">Vous pouvez ensuite utiliser des OpCodes pour identifier les opérations effectuées par le composant, telles que les opérations d’envoi et de réception pour un composant de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="7f632-108">You could then use opcodes to identify the operations that the component performs, such as the send and receive operations for a networking component.</span></span> <span data-ttu-id="7f632-109">Si vous n’avez qu’un seul composant, vous pouvez utiliser la tâche pour refléter une opération majeure dans le composant, telle que la connexion ou la déconnexion, et l’utilisation de l’opcode pour refléter une activité au sein de l’opération, par exemple la lecture du Registre.</span><span class="sxs-lookup"><span data-stu-id="7f632-109">If you had only one component, you could use task to reflect a major operation in the component, such as connect or disconnect, and use opcode to reflect an activity within the operation such as reading the registry.</span></span> <span data-ttu-id="7f632-110">Vous pouvez également utiliser opcode sans spécifier de tâche.</span><span class="sxs-lookup"><span data-stu-id="7f632-110">You could also use opcode without specifying a task.</span></span> <span data-ttu-id="7f632-111">La façon dont vous utilisez des tâches et des OpCodes pour regrouper les événements du consommateur dépend entièrement de vous.</span><span class="sxs-lookup"><span data-stu-id="7f632-111">How you use task and opcodes to group events for the consumer is completely up to you.</span></span>

<span data-ttu-id="7f632-112">Pour définir une tâche, utilisez l’élément **Task** .</span><span class="sxs-lookup"><span data-stu-id="7f632-112">To define a task, use the **task** element.</span></span> <span data-ttu-id="7f632-113">Pour définir un opcode, utilisez l’élément **opcode** .</span><span class="sxs-lookup"><span data-stu-id="7f632-113">To define an opcode, use the **opcode** element.</span></span> <span data-ttu-id="7f632-114">Vous pouvez spécifier jusqu’à 228 OpCodes.</span><span class="sxs-lookup"><span data-stu-id="7f632-114">You can specify up to 228 opcodes.</span></span> <span data-ttu-id="7f632-115">La **valeur** de la tâche doit être supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="7f632-115">The task **value** must be greater than 0.</span></span> <span data-ttu-id="7f632-116">Les OpCodes doivent se trouver dans la plage comprise entre 11 et 239.</span><span class="sxs-lookup"><span data-stu-id="7f632-116">The opcodes must be in the range from 11 through 239.</span></span> <span data-ttu-id="7f632-117">Le fichier Winmeta.xml définit les opérations courantes que vous pouvez utiliser au lieu de définir les vôtres.</span><span class="sxs-lookup"><span data-stu-id="7f632-117">The Winmeta.xml file defines common operations that you can use instead of defining your own.</span></span>

<span data-ttu-id="7f632-118">L’exemple suivant montre comment définir plusieurs tâches et OpCodes.</span><span class="sxs-lookup"><span data-stu-id="7f632-118">The following example shows how to define several tasks and opcodes.</span></span>

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
