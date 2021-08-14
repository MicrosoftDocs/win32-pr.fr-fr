---
description: Vous pouvez importer et exporter des clés symétriques et des clés asymétriques avec CNG. Vous pouvez utiliser les fonctionnalités d’exportation et d’importation de clé pour déplacer des clés entre les machines.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importation et exportation de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907700"
---
# <a name="key-import-and-export"></a>Importation et exportation de clé

Vous pouvez importer et exporter des [*clés symétriques*](/windows/desktop/SecGloss/s-gly) et des clés asymétriques avec CNG. Vous pouvez utiliser les fonctionnalités d’exportation et d’importation de clé pour déplacer des clés entre les machines.

## <a name="symmetric-keys"></a>Clés symétriques

Pour importer ou exporter des clés symétriques (ou de session) dans lesquelles la même clé est utilisée pour chiffrer et déchiffrer des données, vous pouvez utiliser les fonctions [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) et [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) . En règle générale, vous exportez d’abord une clé à l’aide de la fonction **BCryptExportKey** avant l’importation à l’aide de la fonction **BCryptImportKey** . Les fonctions sont conçues pour permettre le chiffrement des clés exportées et importées à l’aide des paramètres *hExportKey* et *hImportKey* ; Toutefois, l’implémentation Microsoft de ces fonctions ne prend pas en charge le chiffrement des clés exportées et importées.

## <a name="asymmetric-keys"></a>Clés asymétriques

Pour importer les paires de clés asymétriques (ou [*publiques/privées*](/windows/desktop/SecGloss/p-gly)) dans lesquelles une clé est utilisée pour chiffrer et l’autre est utilisée pour déchiffrer des données, vous pouvez utiliser l’une des fonctions [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) ou [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) . Un fournisseur CNG doit encoder la paire de clés à l’aide d’un type [*blob de clé*](/windows/desktop/SecGloss/k-gly) pris en charge. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) peut être utilisé pour créer l’objet blob de clé encodé. les [structures CNG](cng-structures.md) décrivent les types et structures BLOB de clé que le fournisseur de clés Microsoft key Stockage prend en charge.

Pour que [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) crée une paire de clés persistante, l’objet blob de clé d’entrée doit contenir une [*clé privée*](/windows/desktop/SecGloss/p-gly). Les [*clés publiques*](/windows/desktop/SecGloss/p-gly) ne sont pas rendues persistantes.

Le nom de clé et la stratégie d’exportation ne font pas partie de la structure d' [*objets BLOB*](/windows/desktop/SecGloss/b-gly) définie dans les [structures CNG](cng-structures.md). Toutefois, si un objet BLOB est d’un type BLOB opaque (tel que l’image mémoire d’un état de clé interne), l’objet BLOB peut contenir les propriétés nom de clé et stratégie d’exportation.

La procédure suivante décrit comment importer une clé privée persistante avec ses propriétés.

**Pour importer une clé persistante**

1.  Créez une clé persistante à l’aide de la fonction [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) .
2.  Définissez les propriétés souhaitées sur l’objet clé à l’aide de la fonction [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) .
3.  Définissez l’objet BLOB de clé d’importation en tant que propriété sur la clé, avec le type d’objet BLOB comme nom de propriété.
4.  Finalisez l’importation de la clé rendue persistante à l’aide de la fonction [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) .

 

 
