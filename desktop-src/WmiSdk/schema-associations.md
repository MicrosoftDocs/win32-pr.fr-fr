---
description: 'Les requêtes d’association de schéma utilisent les mêmes instructions que celles utilisées dans les requêtes d’association de données : les ASSOCIateurs et les références de.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Associations de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210203"
---
# <a name="schema-associations"></a><span data-ttu-id="40632-103">Associations de schéma</span><span class="sxs-lookup"><span data-stu-id="40632-103">Schema Associations</span></span>

<span data-ttu-id="40632-104">Les requêtes d’association de schéma utilisent les mêmes instructions que celles utilisées dans les requêtes d’association de données : les ASSOCIateurs et les références de.</span><span class="sxs-lookup"><span data-stu-id="40632-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="40632-105">Toutefois, avec les requêtes d’association de données, les instances de classe sont retournées et, avec les requêtes d’association de schéma, les noms des classes qui peuvent participer aux relations d’association sont retournés.</span><span class="sxs-lookup"><span data-stu-id="40632-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="40632-106">Par exemple, utilisez une requête de schéma pour rechercher toutes les classes d’association définies dans le schéma qui font référence à une classe source.</span><span class="sxs-lookup"><span data-stu-id="40632-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="40632-107">La syntaxe des ASSOCIateurs et des références d’instructions est la même pour les requêtes d’association de schéma que pour les requêtes d’association de données avec les exceptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="40632-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="40632-108">L’objet source est une classe plutôt qu’une instance.</span><span class="sxs-lookup"><span data-stu-id="40632-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="40632-109">Il existe un mot clé supplémentaire, **SchemaOnly**, qui identifie la requête comme s’appliquant à un schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="40632-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="40632-110">Le mot clé **ClassDefsOnly** n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="40632-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="40632-111">L’exemple suivant illustre la syntaxe complète des ASSOCIateurs d’instruction pour une requête de schéma.</span><span class="sxs-lookup"><span data-stu-id="40632-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="40632-112">Pour plus d’informations sur la syntaxe, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="40632-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



<span data-ttu-id="40632-113">L’exemple suivant montre une requête qui retourne les classes de **protocole** et de **pilote** , les deux classes qui font référence à la classe source.</span><span class="sxs-lookup"><span data-stu-id="40632-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="40632-114">La requête suivante retourne uniquement la classe **Driver** en raison de la restriction placée par le mot clé **AssocClass** .</span><span class="sxs-lookup"><span data-stu-id="40632-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="40632-115">La syntaxe complète des références de l’instruction pour une requête de schéma est la suivante.</span><span class="sxs-lookup"><span data-stu-id="40632-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="40632-116">Pour plus d’informations sur la syntaxe, consultez [références de l’instruction](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="40632-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="40632-117">Les requêtes d’association de schéma peuvent retourner des objets en double.</span><span class="sxs-lookup"><span data-stu-id="40632-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="40632-118">Par exemple, la requête suivante retourne la classe [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) plusieurs fois lors de l’énumération des classes dans l’espace de noms **\\ cimv2 racine** .</span><span class="sxs-lookup"><span data-stu-id="40632-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
