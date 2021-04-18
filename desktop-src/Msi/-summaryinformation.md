---
description: La \_ table SummaryInformation est une table spéciale utilisée avec le flux d’informations de synthèse. Vous pouvez obtenir ou définir le flux d’informations de synthèse d’une base de données Windows Installer en exportant ou en important un fichier d’archive de texte nommé \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519662"
---
# <a name="_summaryinformation"></a><span data-ttu-id="a7d7b-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="a7d7b-104">\_SummaryInformation</span></span>

<span data-ttu-id="a7d7b-105">La \_ table SummaryInformation est une table spéciale utilisée avec le [flux d’informations de synthèse](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a7d7b-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="a7d7b-106">Vous pouvez obtenir ou définir le flux d’informations de synthèse d’une base de données Windows Installer en exportant ou en important un [fichier d’archive de texte](text-archive-files.md) nommé \_ SummaryInformation. IDT.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="a7d7b-107">Le fichier. IDT d’une table SummaryInformation exportée \_ a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="a7d7b-108">La première ligne contient les noms de colonnes de table séparés par des tabulations : PropertyId et value.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="a7d7b-109">Pour obtenir la liste des propriétés et de leurs ID (PID), consultez la rubrique [Propriétés du flux d’informations de synthèse](summary-information-stream-property-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d7b-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="a7d7b-110">La deuxième ligne contient les définitions de colonne séparées par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="a7d7b-111">Les définitions de colonne sont spécifiées de la même façon que dans le [format de fichier d’archive](archive-file-format.md)Basic. IDT.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="a7d7b-112">La colonne PropertyId peut être un entier Short non Nullable.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="a7d7b-113">La colonne valeur peut être une chaîne non Nullable de 255 caractères de long.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="a7d7b-114">La troisième ligne est le nom de la table et le nom de la colonne de clé primaire, séparés par des tabulations : \_ SummaryInformation et PropertyId.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="a7d7b-115">Les lignes restantes dans le fichier représentent le PID et la valeur associée, séparés par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="a7d7b-116">La date et l’heure dans \_ SummaryInformation sont au format suivant : aaaa/mm/jj hh :: mm :: SS.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="a7d7b-117">Par exemple, 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="a7d7b-118">Voici un exemple de [flux d’informations résumées](summary-information-stream.md) d’une base de données au format. IDT.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="a7d7b-119">Lorsque vous utilisez [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou la méthode [Import](database-import.md) de l’objet [**Database**](database-object.md) pour importer une table d’archive de texte nommée \_ SummaryInformation dans une base de données du programme d’installation, vous écrivez le flux « 05SummaryInformation » dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



