---
description: 'En savoir plus sur : colonnes définies par l’utilisateur'
title: Colonnes définies par l’utilisateur
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034237"
---
# <a name="user-defined-columns"></a><span data-ttu-id="074de-103">Colonnes définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="074de-103">User Defined Columns</span></span>


<span data-ttu-id="074de-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="074de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="074de-105">Colonnes définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="074de-105">User Defined Columns</span></span>

<span data-ttu-id="074de-106">Les colonnes définies par l’utilisateur sont des colonnes dont les valeurs par défaut sont fournies par une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="074de-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="074de-107">Ces colonnes sont toujours marquées et définies sur la valeur calculée par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="074de-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="074de-108">Cette valeur doit être stable pour chaque ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="074de-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="074de-109">La fonction de rappel est utilisée uniquement lorsque l’application ou le moteur de base de données lui-même doit lire la valeur de la colonne pour une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="074de-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="074de-110">L’application a la possibilité de remplacer la valeur par défaut et de définir une valeur spécifique dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="074de-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="074de-111">Lorsque la valeur par défaut est remplacée dans les colonnes, elle utilise de l’espace dans la ligne ; sinon, les colonnes par défaut définies par l’utilisateur n’utilisent pas d’espace dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="074de-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="074de-112">L’option valeurs par défaut définies par l’utilisateur est définie dans le membre **Grbit** de la structure [JET_COLUMNDEF](./jet-columndef-structure.md) dans l’appel à [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="074de-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="074de-113">Le paramètre *pvDefault* de la fonction [JetAddColumn](./jetaddcolumn-function.md) pointe vers une structure [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , qui contient le nom de la fonction de rappel dans le membre **szCallback** et les données qui sont passées au rappel dans le membre **pbUserData** .</span><span class="sxs-lookup"><span data-stu-id="074de-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
