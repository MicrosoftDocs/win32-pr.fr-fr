---
title: Scripts de valeurs séparées par des virgules (CSV)
description: Windows 2000 comprend un utilitaire de ligne de commande, CSVDE, pour importer des objets d’annuaire à l’aide de fichiers de .csv et exporter des objets d’annuaire en tant que fichiers .csv.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Scripts de valeurs séparées par des virgules Active Directory
- Scripts, valeur de valeurs séparées par des virgules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095165"
---
# <a name="comma-separated-value-csv-scripts"></a>Scripts de valeurs séparées par des virgules (CSV)

Windows 2000 comprend un utilitaire de ligne de commande, CSVDE, pour importer des objets d’annuaire à l’aide de fichiers de .csv et exporter des objets d’annuaire en tant que fichiers .csv. Les scripts CSV sont créés à des fins de facilité d’utilisation. La première ligne du script identifie les attributs dans les lignes qui suivent. Les colonnes sont séparées par des virgules. le format de fichier est compatible avec le format de .csv Microsoft Excel, afin que les fichiers soient facilement créés. utilisez Excel ou tout autre outil capable de lire et d’écrire des fichiers .csv. CSVDE prend en charge Unicode.

## <a name="example-csv-file"></a>Exemple de fichier CSV

L’exemple de code suivant est un fichier CSV qui ajoute une classe auxiliaire.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




