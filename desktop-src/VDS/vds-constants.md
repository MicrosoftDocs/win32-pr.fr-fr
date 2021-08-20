---
description: Constantes VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Constantes VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9fa0c6196e1085de3a5433750b890e2ad3bc42f4a86022587f02157521eacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125692"
---
# <a name="vds-constants"></a>Constantes VDS

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Les constantes VDS sont classées comme suit :

-   [Constantes d’état d’objet](#object-status-constants)
-   [Constantes d’indicateurs automagic](#automagic-hints-constants)
-   [Constantes diverses](#miscellaneous-constants)

### <a name="object-status-constants"></a>Constantes d’état d’objet



| Constante           | Valeur |
|--------------------|-------|
| ÉTAT \_ inconnu    | 0     |
| ÉTAT \_ en ligne     | 1     |
| ÉTAT \_ non \_ prêt | 2     |
| ÉTAT \_ aucun \_ support  | 3     |
| ÉTAT \_ hors connexion    | 4     |
| échec de l’état \_     | 5     |
| ÉTAT \_ manquant    | 6     |



 

### <a name="automagic-hints-constants"></a>Constantes d’indicateurs automagic



| Constante                               | Valeur   |
|----------------------------------------|---------|
| MOSTLYREADS de l' \_ indicateur VDS \_                 | 0x0002L |
| OPTIMIZEFORSEQUENTIALREADS de l' \_ indicateur VDS \_  | 0x0004L |
| OPTIMIZEFORSEQUENTIALWRITES de l' \_ indicateur VDS \_ | 0x0008L |
| REMAPENABLED de l' \_ indicateur VDS \_                | 0x0020L |
| WRITETHROUGHCACHINGENABLED de l' \_ indicateur VDS \_  | 0x0040L |
| HARDWARECHECKSUMENABLED de l' \_ indicateur VDS \_     | 0x0080L |
| ISYANKABLE de l' \_ indicateur VDS \_                  | 0x0100L |



 

### <a name="miscellaneous-constants"></a>Constantes diverses



| Constante                     | Valeur      |
|------------------------------|------------|
| \_priorité de \_ reconstruction \_ minimale de VDS  | 0x0001L    |
| \_ \_ informations sur le numéro d’unité logique VDS \_   | 1          |
| longueur maximale du \_ nom d’ordinateur \_    | 15         |
| \_longueur max PROVIDERNAME \_    | 200        |
| longueur maximale de \_ VERSIONSTRING \_   | 16         |
| lettre de lecteur \_ \_ prop          | N/A        |
| \_taille de \_ nom \_ FS max.          | 8          |
| \_idx de membre non valide \_         | 0xFFFFFFFF |
| longueur du nom de la \_ partition GPT \_ \_ | 36         |
| \_chemin d’accès maximal                    | 260        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence VDS](vds-reference.md)
</dt> </dl>

 

 
