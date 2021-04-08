---
title: Scripts de valeurs séparées par des virgules (CSV)
description: Windows 2000 comprend un utilitaire de ligne de commande, CSVDE, qui permet d’importer des objets d’annuaire à l’aide de fichiers. csv et d’exporter des objets d’annuaire en tant que fichiers. csv.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Scripts de valeurs séparées par des virgules Active Directory
- Scripts, valeur de valeurs séparées par des virgules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671001"
---
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="74a4e-105">Scripts de valeurs séparées par des virgules (CSV)</span><span class="sxs-lookup"><span data-stu-id="74a4e-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="74a4e-106">Windows 2000 comprend un utilitaire de ligne de commande, CSVDE, qui permet d’importer des objets d’annuaire à l’aide de fichiers. csv et d’exporter des objets d’annuaire en tant que fichiers. csv.</span><span class="sxs-lookup"><span data-stu-id="74a4e-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="74a4e-107">Les scripts CSV sont créés à des fins de facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="74a4e-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="74a4e-108">La première ligne du script identifie les attributs dans les lignes qui suivent.</span><span class="sxs-lookup"><span data-stu-id="74a4e-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="74a4e-109">Les colonnes sont séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="74a4e-109">Columns are separated by commas.</span></span> <span data-ttu-id="74a4e-110">Le format de fichier est compatible avec le format Microsoft Excel. csv, afin que les fichiers soient facilement créés.</span><span class="sxs-lookup"><span data-stu-id="74a4e-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="74a4e-111">Utilisez Excel ou tout autre outil capable de lire et d’écrire des fichiers. csv.</span><span class="sxs-lookup"><span data-stu-id="74a4e-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="74a4e-112">CSVDE prend en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="74a4e-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="74a4e-113">Exemple de fichier CSV</span><span class="sxs-lookup"><span data-stu-id="74a4e-113">Example CSV File</span></span>

<span data-ttu-id="74a4e-114">L’exemple de code suivant est un fichier CSV qui ajoute une classe auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="74a4e-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




