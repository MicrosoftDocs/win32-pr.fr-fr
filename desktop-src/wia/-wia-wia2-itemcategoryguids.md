---
description: Les éléments WIA (Windows Image Acquisition) 2,0 sont regroupés en catégories qui définissent la façon dont un IWiaItem2 doit être traité ou utilisé.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID de catégorie d’élément WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544673"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="5d08a-103">GUID de catégorie d’élément WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="5d08a-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="5d08a-104">Les éléments WIA (Windows Image Acquisition) 2,0 sont regroupés en catégories qui définissent la façon dont un [**IWiaItem2**](-wia-iwiaitem2.md) doit être traité ou utilisé.</span><span class="sxs-lookup"><span data-stu-id="5d08a-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="5d08a-105">Par exemple, si l’élément représente un flux, l’application doit s’attendre à ce qu’il contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="5d08a-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="5d08a-106">Si l’élément représente un fichier fini, une application WIA 2,0 doit la traiter ainsi, en supposant que les données sont statiques et situées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5d08a-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="5d08a-107">(Les règles pour chaque élément sont définies dans leurs documents de spécification individuels.) Chaque catégorie a une constante de type GUID.</span><span class="sxs-lookup"><span data-stu-id="5d08a-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="5d08a-108">Constante</span><span class="sxs-lookup"><span data-stu-id="5d08a-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="5d08a-109">Description</span><span class="sxs-lookup"><span data-stu-id="5d08a-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="5d08a-110"><dt>**WIA \_ catégorie \_ auto**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="5d08a-111">Élément qui représente les paramètres de configuration automatique pour un périphérique de scanneur WIA 2,0 qui prend en charge l’analyse configurée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5d08a-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="5d08a-112"><dt>**\_chargeur de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="5d08a-113">Élément de chargeur qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge les flux de documents.</span><span class="sxs-lookup"><span data-stu-id="5d08a-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="5d08a-114"><dt>**\_retour du \_ chargeur de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="5d08a-115">Source de données programmable décrivant la source de données de l’arrière-plan d’un élément de chargeur de base duplex.</span><span class="sxs-lookup"><span data-stu-id="5d08a-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="5d08a-116"><dt>**\_chargeur de catégorie WIA \_ \_ avant**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="5d08a-117">Source de données programmable décrivant la source de données frontale d’un élément de chargeur de base duplex.</span><span class="sxs-lookup"><span data-stu-id="5d08a-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="5d08a-118"><dt>**\_film de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="5d08a-119">Élément de film qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge les unités de numérisation de film.</span><span class="sxs-lookup"><span data-stu-id="5d08a-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="5d08a-120"><dt>**\_fichier de catégorie WIA \_ terminé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="5d08a-121">Élément qui n’est pas une source de données programmable, ou élément qui fournit des données dans un format de fichier terminé, ou un élément de dossier qui contient les éléments de format de fichier terminés.</span><span class="sxs-lookup"><span data-stu-id="5d08a-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="5d08a-122"><dt>**\_plateau de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="5d08a-123">Élément à plat qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge l’analyse du plateau à plat.</span><span class="sxs-lookup"><span data-stu-id="5d08a-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="5d08a-124"><dt>**\_dossier de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="5d08a-125">Un élément de stockage de dossier (pas une source de données programmable) contenant d’autres éléments de dossier ou des fichiers finis, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="5d08a-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="5d08a-126"><dt>**\_racine de catégorie WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="5d08a-127">Élément racine de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5d08a-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="5d08a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d08a-128">Requirements</span></span>



| <span data-ttu-id="5d08a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d08a-129">Requirement</span></span> | <span data-ttu-id="5d08a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d08a-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d08a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d08a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5d08a-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d08a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5d08a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d08a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5d08a-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d08a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d08a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d08a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d08a-136"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d08a-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




