---
title: Définition des mots clés utilisés pour classer les types d’événements
description: Les fournisseurs utilisent des mots clés pour classer différents types d’événements.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103841978"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Définition des mots clés utilisés pour classer les types d’événements

Les fournisseurs utilisent des mots clés pour classer différents types d’événements. Par exemple, vous pouvez créer un mot clé pour tous les événements de lecture, puis appliquer le mot clé Read à tout événement qui effectue une opération de lecture telle que la lecture à partir d’un fichier ou d’un registre. Les consommateurs peuvent ensuite utiliser les valeurs de bits de mot clé pour filtrer différentes classifications d’événements. Par exemple, le consommateur peut demander tous les événements de lecture ou tous les événements de lecture de la tâche X (si vous regroupez également les événements par tâche). Pour définir un mot clé, utilisez l’élément de **mot clé** .

Une session de suivi ETW peut utiliser les mots clés (de la même façon qu’elle utilise le niveau) pour limiter les événements que le service ETW écrit dans son fichier journal de suivi d’événements. Une session de suivi peut activer le fournisseur à l’aide de deux ensembles de masques de réinitialisation de mot clé : un masque de bits « any » dans lequel l’événement est écrit si l’un des bits de mot clé de l’événement correspond à l’un des bits définis dans ce masque, et un masque de bits « All » pour les événements correspondant au cas « any », l’événement est écrit uniquement si tous les bits du masque « All » existent dans le masque de bits du mot clé de l’événement

Par exemple, si le fournisseur définit un événement qui spécifie un mot clé Read (bit 0) et un mot clé d’accès local (bit 1), et un deuxième événement qui spécifie un mot clé de lecture (bit 0) et un mot clé d’accès à distance (bit 2), vous pouvez définir le masque de bits « tout » sur 1 pour recevoir tous les événements de lecture, ou vous pouvez définir le masque de bits « tout » sur 1 et le masque de bits « tous » sur 3 pour recevoir uniquement les lectures locales.

Vous devez spécifier les attributs **Name** et **Mask** du mot clé. Le masque ne doit définir qu’un seul bit, entre le bit 0 et le bit 47. Les bits 48 à 64 sont réservés.

Les attributs **symbol** et **message** sont facultatifs.

L’exemple suivant montre comment définir un mot clé.

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
