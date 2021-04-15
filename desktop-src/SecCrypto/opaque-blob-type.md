---
description: Les objets BLOB opaques, également appelés OPAQUEKEYBLOBs, sont utilisés pour stocker les clés de session dans un format spécifique au fournisseur, tel que Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Type d’objet BLOB opaque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393768"
---
# <a name="opaque-blob-type"></a>Type d’objet BLOB opaque

Les [*objets BLOB opaques*](../secgloss/o-gly.md), également appelés OPAQUEKEYBLOBs, sont utilisés pour stocker les [*clés de session*](../secgloss/s-gly.md) dans un format spécifique au fournisseur, tel que [*Schannel*](../secgloss/s-gly.md). Ils contiennent le matériel de clé de base et toutes les informations d' [*État*](../secgloss/s-gly.md) actuelles. Cela comprend des informations telles que la [*valeur Salt*](../secgloss/s-gly.md), le [*vecteur d’initialisation*](../secgloss/i-gly.md)et la table clé. Le format des objets BLOB opaques n’est pas publié. Chaque fournisseur de services de chiffrement détermine son propre format d’objet BLOB.

Étant donné qu’une clé est exportée dans un objet BLOB opaque dans un format spécifique au CSP, elle ne peut être importée que dans le CSP à partir duquel elle a été exportée à l’origine.

Lorsque deux processus sont impliqués, chaque [*processus*](../secgloss/p-gly.md) appelle [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) indépendamment. Chaque processus obtient un handle vers un conteneur de clé. Il est possible que les deux processus aient des handles vers le même conteneur de clé. Un processus crée les clés et les exporte dans des objets BLOB opaques, puis transmet les objets BLOB au deuxième processus. Le deuxième processus importe les clés de l’objet BLOB dans son [*conteneur de clé*](../secgloss/k-gly.md).

Si un fournisseur de services de chiffrement de matériel ne prend pas en charge l’exportation des clés, l’objet BLOB peut uniquement contenir l’index d’un registre de clés, ou un nom similaire. Dans ce cas, le reste de la procédure est ignoré.

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
