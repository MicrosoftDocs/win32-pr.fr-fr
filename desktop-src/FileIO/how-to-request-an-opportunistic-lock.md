---
description: Les verrous opportunistes sont demandés en ouvrant un fichier avec les autorisations et les indicateurs appropriés à l’application ouvrant le fichier. Tous les fichiers pour lesquels des verrous opportunistes seront demandés doivent être ouverts pour une opération avec chevauchement (asynchrone).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Comment demander un verrou opportuniste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009929"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Comment demander un verrou opportuniste

Les applications clientes demandent directement des verrous opportunistes uniquement lorsque le verrou est destiné à un fichier sur le serveur local. Lors de l’accès aux fichiers sur des serveurs distants, il s’agit du redirecteur réseau, et non de l’application cliente, qui demande le verrou opportuniste du serveur distant.

Les verrous opportunistes sont demandés en ouvrant un fichier avec les autorisations et les indicateurs appropriés à l’application ouvrant le fichier. Tous les fichiers pour lesquels des verrous opportunistes seront demandés doivent être ouverts pour une opération avec chevauchement (asynchrone). Une fois les fichiers ouverts pour une opération avec chevauchement, utilisez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec le code de contrôle approprié pour demander un verrou opportuniste. Pour obtenir la liste des opérations de verrouillage opportuniste, voir [opérations de verrouillage opportuniste](opportunistic-lock-operations.md).

Les applications sont averties qu’un verrou opportuniste est interrompu à l’aide du membre **hEvent** de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associée au fichier. Les applications peuvent également utiliser des fonctions telles que [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) et [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted). L’application est chargée d’associer le fichier approprié au verrou opportuniste rompu.

Pour plus d’informations sur la notification, consultez [Synchronization](/windows/desktop/Sync/synchronization).

 

 
