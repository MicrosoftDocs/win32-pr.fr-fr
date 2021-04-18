---
description: Le programme d’installation fournit des fonctions qui manipulent les enregistrements dans une base de données d’installation. Ces fonctions peuvent être utilisées conjointement avec les fonctions décrites dans utilisation de requêtes pour apporter des modifications réelles dans une base de données.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Utilisation des enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542951"
---
# <a name="working-with-records"></a><span data-ttu-id="a0e40-104">Utilisation des enregistrements</span><span class="sxs-lookup"><span data-stu-id="a0e40-104">Working with Records</span></span>

<span data-ttu-id="a0e40-105">Le programme d’installation fournit des fonctions qui manipulent les enregistrements dans une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="a0e40-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="a0e40-106">Ces fonctions peuvent être utilisées conjointement avec les fonctions décrites dans [utilisation de requêtes](working-with-queries.md) pour apporter des modifications réelles dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="a0e40-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="a0e40-107">Les fonctions suivantes créent ou suppriment des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="a0e40-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="a0e40-108">Pour créer un nouvel enregistrement pour une base de données, appelez la fonction [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="a0e40-109">Pour effacer les données d’un enregistrement, attribuez la valeur null à chaque champ en appelant la fonction [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="a0e40-110">Les fonctions suivantes remplissent les champs d’enregistrements spécifiés :</span><span class="sxs-lookup"><span data-stu-id="a0e40-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="a0e40-111">Pour définir un enregistrement sur un entier, appelez la fonction [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="a0e40-112">Pour définir un enregistrement sur une chaîne, appelez la fonction [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="a0e40-113">Pour insérer un fichier entier dans un champ de flux, appelez la fonction [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="a0e40-114">Les fonctions suivantes lisent des valeurs à partir de champs d’enregistrements spécifiés :</span><span class="sxs-lookup"><span data-stu-id="a0e40-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="a0e40-115">Pour lire une valeur entière à partir d’un champ, appelez la fonction [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="a0e40-116">Pour récupérer une valeur de chaîne, appelez la fonction [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="a0e40-117">Pour obtenir un flux, appelez la fonction [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="a0e40-118">Pour déterminer si un champ particulier d’un enregistrement a la valeur null, appelez la fonction [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="a0e40-119">Les fonctions suivantes sont des fonctions d’enregistrement d’informations :</span><span class="sxs-lookup"><span data-stu-id="a0e40-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="a0e40-120">Pour obtenir le nombre de champs qu’un enregistrement contient, appelez la fonction [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="a0e40-121">Pour obtenir la taille d’un champ, appelez la fonction [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) .</span><span class="sxs-lookup"><span data-stu-id="a0e40-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="a0e40-122">La valeur de retour de **MsiRecordDataSize** est sensible au type de champ.</span><span class="sxs-lookup"><span data-stu-id="a0e40-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



