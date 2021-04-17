---
title: Identification du fournisseur
description: Un manifeste peut identifier un ou plusieurs fournisseurs. Pour identifier un fournisseur, utilisez l’élément Provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507839"
---
# <a name="identifying-the-provider"></a>Identification du fournisseur

Un manifeste peut identifier un ou plusieurs fournisseurs. Pour identifier un fournisseur, utilisez l’élément **Provider** . Vous devez spécifier les attributs **Name**, **GUID**, **resourceFileName**, **messageFileName** et **symbol** . Si vous localisez votre manifeste, vous devez également spécifier l’attribut de **message** , que les consommateurs utilisent comme afficher le nom du fournisseur. Si vous ne spécifiez pas l’attribut de **message** , les consommateurs utilisent la valeur de l’attribut **Name** .

Vous pouvez identifier jusqu’à 16 fournisseurs dans le manifeste. Si vous souhaitez identifier plus de 16 fournisseurs, vous devez inclure la section **messageTable** du manifeste que les fournisseurs dix-septième et on doit utiliser pour assigner des valeurs de ressource pour les chaînes de message qu’ils définissent : la table de messages ne doit pas inclure de chaînes de message que les fournisseurs 1 à 16 sont définis.

L’exemple suivant montre comment utiliser l’élément **Provider** pour identifier un fournisseur.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
