---
title: Macros Wrapper TraceLogging
description: Répertorie les macros wrapper pour les fournisseurs TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bad266f44dbd82c31ceea95eed2978c5634beb8a75830d073465ef11c1be331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966478"
---
# <a name="tracelogging-wrapper-macros"></a>Macros Wrapper TraceLogging

Répertorie les macros wrapper pour les fournisseurs TraceLogging.

Pour enregistrer des événements à l’aide des fournisseurs TraceLogging, vous devez utiliser le TraceLogging écrire des macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) ou [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity). Ces deux macros vous obligent à encapsuler les données d’événement dans une macro wrapper. Il existe plusieurs macros Wrapper différentes pour différents types de données. Pour obtenir la liste complète des macros TraceLogging, consultez [macros TraceLogging](trace-logging-macros.md).

Outre les macros Wrapper ci-dessus, plusieurs macros sont disponibles pour les types de données individuels. Toutes ces macros ont le même format que la macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) . Vous pouvez utiliser la macro TraceLoggingValue pour détecter automatiquement la macro Wrapper appropriée à utiliser, ou utiliser la macro spécifique directement.

-   [**TraceLoggingBinary**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [**TraceLoggingChannel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [**TraceLoggingCustomAttribute**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [**TraceLoggingDescription**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [**TraceLoggingEventTag**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [**TraceLoggingKeyword**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [**TraceLoggingLevel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [**TraceLoggingOpcode**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [**TraceLoggingSocketAddress**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [**TraceLoggingStruct**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [**TraceLoggingValue**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> **TraceLoggingOptionGroup** est spécifiquement destiné à être utilisé dans TRACELOGGING \_ définir le \_ fournisseur.
>
> -   [**TraceLoggingOptionGroup**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

Voici les macros Wrapper individuelles.

-   TraceLoggingInt8

-   TraceLoggingUInt8

-   TraceLoggingInt16

-   TraceLoggingUInt16

-   TraceLoggingInt32

-   TraceLoggingUInt32

-   TraceLoggingInt64

-   TraceLoggingUInt64

-   TraceLoggingFloat32

-   TraceLoggingFloat64

-   TraceLoggingBool

-   TraceLoggingFileTime

-   TraceLoggingGuid

-   TraceLoggingPointer

-   TraceLoggingSystemTime

-   TraceLoggingHexInt8

-   TraceLoggingHexUInt8

-   TraceLoggingHexInt32

-   TraceLoggingHexUInt32

-   TraceLoggingHexInt64

-   TraceLoggingHexUInt64

-   TraceLoggingWchar

-   TraceLoggingChar

-   TraceLoggingIntPtr

-   TraceLoggingUIntPtr

-   TraceLoggingBoolean

-   TraceLoggingHexInt16

-   TraceLoggingHexUInt16

-   TraceLoggingPid

-   TraceLoggingTid

-   TraceLoggingPort

-   TraceLoggingWinError

-   TraceLoggingNTStatus

-   TraceLoggingHResult

-   TraceLoggingSocketAddress

-   TraceLoggingSid

-   TraceLoggingString

-   TraceLoggingWideString

-   TraceLoggingCountedString

-   TraceLoggingCountedWideString

-   TraceLoggingAnsiString

-   TraceLoggingUnicodeString

-   TraceLoggingBinary (void \* Data, taille des données en octets, \[ facultatif \] Name) les paramètres de cette macro diffèrent de ceux ci-dessus. Si le paramètre *Name* est spécifié, il doit s’agir d’un littéral de chaîne (et non d’une variable) et ne peut pas contenir de caractères null incorporés. Si le paramètre *Name* n’est pas fourni, un nom est généré automatiquement.

L’API TraceLogging rend également plusieurs macros disponibles pour les tableaux. Ces tableaux peuvent avoir une longueur fixe ou être d’une longueur variable, en fonction de la macro wrapper que vous choisissez d’utiliser. Toutes ces macros Wrapper suivent ce format.

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

Le paramètre *pVals* pointe vers le tableau de données et *cVals* indique le nombre d’éléments dans le tableau. *cVals* doit être une constante et ne peut pas être une variable. Comme avec les macros wrapper à valeur unique, *Name*, **desc** et *Tags* sont des paramètres facultatifs et doivent respecter les mêmes restrictions que celles expliquées avec la macro **TraceLoggingValue** .

-   TraceLoggingInt8FixedArray

-   TraceLoggingUInt8FixedArray

-   TraceLoggingInt16FixedArray

-   TraceLoggingUInt16FixedArray

-   TraceLoggingInt32FixedArray

-   TraceLoggingUInt32FixedArray

-   TraceLoggingInt64FixedArray

-   TraceLoggingUInt64FixedArray

-   TraceLoggingFloat32FixedArray

-   TraceLoggingFloat64FixedArray

-   TraceLoggingBoolFixedArray

-   TraceLoggingGuidFixedArray

-   TraceLoggingPointerFixedArray

-   TraceLoggingFileTimeFixedArray

-   TraceLoggingSystemTimeFixedArray

-   TraceLoggingHexInt8FixedArray

-   TraceLoggingHexUInt8FixedArray

-   TraceLoggingHexInt32FixedArray

-   TraceLoggingHexUInt32FixedArray

-   TraceLoggingHexInt64FixedArray

-   TraceLoggingHexUInt64FixedArray

-   TraceLoggingWcharFixedArray

-   TraceLoggingCharFixedArray

-   TraceLoggingIntPtrFixedArray

-   TraceLoggingUIntPtrFixedArray

-   TraceLoggingBooleanFixedArray

-   TraceLoggingHexInt16FixedArray

-   TraceLoggingHexUInt16FixedArray

-   TraceLoggingInt8Array

-   TraceLoggingUInt8Array

-   TraceLoggingInt16Array

-   TraceLoggingUInt16Array

-   TraceLoggingInt32Array

-   TraceLoggingUInt32Array

-   TraceLoggingInt64Array

-   TraceLoggingUInt64Array

-   TraceLoggingFloat32Array

-   TraceLoggingFloat64Array

-   TraceLoggingBoolArray

-   TraceLoggingGuidArray

-   TraceLoggingPointerArray

-   TraceLoggingFileTimeArray

-   TraceLoggingSystemTimeArray

-   TraceLoggingHexInt8Array

-   TraceLoggingHexUInt8Array

-   TraceLoggingHexInt32Array

-   TraceLoggingHexUInt32Array

-   TraceLoggingHexInt64Array

-   TraceLoggingHexUInt64Array

-   TraceLoggingWcharArray

-   TraceLoggingCharArray

-   TraceLoggingIntPtrArray

-   TraceLoggingUIntPtrArray

-   TraceLoggingBooleanArray

-   TraceLoggingHexInt16Array

-   TraceLoggingHexUInt16Array

 

 




