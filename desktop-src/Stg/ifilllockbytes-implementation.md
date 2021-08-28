---
title: IFillLockBytes-implémentation
description: Le système fournit une implémentation de IFillLockBytes dans le cadre de l’implémentation de fichiers composés.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663019"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes-implémentation

Le système fournit une implémentation de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) dans le cadre de l’implémentation de fichiers composés.

Le téléchargement de code peut créer une instance d’un objet de fichier composé asynchrone en appelant [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes). Le téléchargement de code peut également créer une instance d’un objet wrapper de tableau d’octets asynchrone sur un fichier ou un tableau d’octets existant en appelant la fonction [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) ou la fonction [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .

## <a name="when-to-use"></a>Quand l’utiliser

Actuellement, les monikers d’URL sont les seuls utilisateurs de l’implémentation de stockage asynchrone COM.

## <a name="remarks"></a>Remarques

Voici les quatre méthodes de l’implémentation de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Écrit un nouveau bloc d’octets à la fin d’un tableau d’octets. La taille du bloc est spécifiée en tant que paramètre de [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Écrit un nouveau bloc de données à un emplacement spécifié dans le tableau d’octets.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

Définit la taille du tableau d’octets. Retourne E \_ Fail à partir des appels à [**ILockBytes :: readatum**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) qui tentent d’accéder aux données au-delà de la limite supérieure spécifiée par la méthode.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes :: Terminate**
</dt> <dd>

Informe le tableau d’octets qu’un téléchargement a été terminé, avec succès ou non.

</dd> </dl>

 

 




