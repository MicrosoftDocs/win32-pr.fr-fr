---
title: Définition des tâches et des OpCodes
description: Les fournisseurs utilisent des tâches et des OpCodes pour regrouper logiquement les événements. Le regroupement d’événements permet aux consommateurs de rechercher uniquement les événements qui contiennent des combinaisons tâche et opcode spécifiques.
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb576251edf4de14c564c6e468209ece93e5840da9e0d821c20b132794f48ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032469"
---
# <a name="defining-tasks-and-opcodes"></a>Définition des tâches et des OpCodes

Les fournisseurs utilisent des tâches et des OpCodes pour regrouper logiquement les événements. Le regroupement d’événements permet aux consommateurs de rechercher uniquement les événements qui contiennent des combinaisons tâche et opcode spécifiques. En règle générale, vous utilisez des tâches pour identifier un composant majeur du fournisseur, tel que le réseau ou le composant de base de données. Vous pouvez ensuite utiliser des OpCodes pour identifier les opérations effectuées par le composant, telles que les opérations d’envoi et de réception pour un composant de mise en réseau. Si vous n’avez qu’un seul composant, vous pouvez utiliser la tâche pour refléter une opération majeure dans le composant, telle que la connexion ou la déconnexion, et l’utilisation de l’opcode pour refléter une activité au sein de l’opération, par exemple la lecture du Registre. Vous pouvez également utiliser opcode sans spécifier de tâche. La façon dont vous utilisez des tâches et des OpCodes pour regrouper les événements du consommateur dépend entièrement de vous.

Pour définir une tâche, utilisez l’élément **Task** . Pour définir un opcode, utilisez l’élément **opcode** . Vous pouvez spécifier jusqu’à 228 OpCodes. La **valeur** de la tâche doit être supérieure à 0. Les OpCodes doivent se trouver dans la plage comprise entre 11 et 239. Le fichier Winmeta.xml définit les opérations courantes que vous pouvez utiliser au lieu de définir les vôtres.

L’exemple suivant montre comment définir plusieurs tâches et OpCodes.

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
