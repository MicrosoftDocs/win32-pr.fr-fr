---
description: La méthode FormatRecord de l’objet session retourne une chaîne mise en forme à partir d’un modèle et des données d’enregistrement.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. FormatRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528506"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="12880-103">Session. FormatRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="12880-103">Session.FormatRecord method</span></span>

<span data-ttu-id="12880-104">La méthode **FormatRecord** de l’objet [**session**](session-object.md) retourne une chaîne mise en forme à partir d’un modèle et des données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="12880-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="12880-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12880-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="12880-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12880-107">*enregistrement*</span><span class="sxs-lookup"><span data-stu-id="12880-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="12880-108">Objet **Record** requis contenant un modèle et des données à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="12880-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="12880-109">La chaîne de modèle doit être définie dans le champ 0, suivi de tous les paramètres de données référencés.</span><span class="sxs-lookup"><span data-stu-id="12880-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12880-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12880-110">Return value</span></span>

<span data-ttu-id="12880-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="12880-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12880-112">Notes</span><span class="sxs-lookup"><span data-stu-id="12880-112">Remarks</span></span>

<span data-ttu-id="12880-113">La méthode **FormatRecord** utilise le processus de format suivant.</span><span class="sxs-lookup"><span data-stu-id="12880-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="12880-114">Les paramètres à mettre [en forme](formatted.md) sont placés entre crochets \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="12880-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="12880-115">Les crochets peuvent être itérés, car les substitutions sont résolues de l’intérieur vers l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="12880-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="12880-116">Si une partie de la chaîne est entourée d’accolades {} et ne contient aucun crochet, la partie reste inchangée, y compris les accolades.</span><span class="sxs-lookup"><span data-stu-id="12880-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="12880-117">Si une partie de la chaîne est placée entre accolades et contient un ou plusieurs noms de propriété, et si toutes les propriétés sont trouvées, le texte (avec les substitutions résolues) s’affiche sans les accolades.</span><span class="sxs-lookup"><span data-stu-id="12880-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="12880-118">Si l’une des propriétés est introuvable, tout le texte entre les accolades et les accolades elles-mêmes sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="12880-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="12880-119">**Pour mettre en forme des chaînes à l’aide de la méthode FormatRecord**</span><span class="sxs-lookup"><span data-stu-id="12880-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="12880-120">Les paramètres numériques sont remplacés en remplaçant le marqueur par la valeur du champ d’enregistrement correspondant, avec des valeurs manquantes ou null qui ne génèrent pas de texte.</span><span class="sxs-lookup"><span data-stu-id="12880-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="12880-121">La chaîne résultante est traitée en remplaçant les paramètres non-enregistrement par les valeurs correspondantes, comme indiqué dans les descriptions suivantes.</span><span class="sxs-lookup"><span data-stu-id="12880-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="12880-122">Si une sous-chaîne se présentant sous la forme « \[ PropertyName \] » est rencontrée, elle est remplacée par la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="12880-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="12880-123">Si une sous-chaîne du formulaire « \[ % EnvironmentVariable \] » est trouvée, la valeur de la variable d’environnement est remplacée.</span><span class="sxs-lookup"><span data-stu-id="12880-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="12880-124">Si une sous-chaîne du formulaire \[ \# *filekey* \] est trouvée, elle est remplacée par le chemin d’accès complet du fichier, avec la valeur *filekey* utilisée comme clé dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="12880-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="12880-125">La valeur de \[ \# *filekey* \] reste vide et n’est pas remplacée par un chemin d’accès jusqu’à ce que le programme d’installation exécute l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="12880-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="12880-126">La valeur de \[ \# *filekey* \] dépend de l’état d’installation du composant auquel le fichier appartient.</span><span class="sxs-lookup"><span data-stu-id="12880-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="12880-127">Si le composant est exécuté à partir de la source, la valeur est le chemin d’accès à l’emplacement source du fichier.</span><span class="sxs-lookup"><span data-stu-id="12880-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="12880-128">Si le composant est exécuté localement, la valeur est le chemin d’accès à l’emplacement cible du fichier après l’installation.</span><span class="sxs-lookup"><span data-stu-id="12880-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="12880-129">Si le composant est absent, le chemin d’accès est vide.</span><span class="sxs-lookup"><span data-stu-id="12880-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="12880-130">Pour plus d’informations sur la vérification de l’état d’installation des composants, consultez [vérification de l’installation de fonctionnalités, de composants et de fichiers](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="12880-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="12880-131">Si une sous-chaîne du formulaire \[ *$componentkey* \] est trouvée, elle est remplacée par le répertoire d’installation du composant, avec la valeur *componentkey* utilisée comme clé dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="12880-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="12880-132">La valeur de \[ $ *componentkey* \] reste vide et n’est pas remplacée par un répertoire tant que le programme d’installation n’a pas exécuté l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="12880-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="12880-133">La valeur de \[ $ *componentkey* \] dépend de l’état d’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="12880-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="12880-134">Si le composant est exécuté à partir de la source, la valeur est le répertoire source du fichier.</span><span class="sxs-lookup"><span data-stu-id="12880-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="12880-135">Si le composant est exécuté localement, la valeur est le répertoire cible après l’installation.</span><span class="sxs-lookup"><span data-stu-id="12880-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="12880-136">Si le composant est absent, la valeur est laissée vide.</span><span class="sxs-lookup"><span data-stu-id="12880-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="12880-137">Pour plus d’informations sur la vérification de l’état d’installation des composants, consultez [vérification de l’installation de fonctionnalités, de composants et de fichiers](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="12880-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="12880-138">Si une sous-chaîne du formulaire « \[ \\ c \] » est trouvée, elle est remplacée par le caractère sans traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="12880-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="12880-139">Seul le premier caractère après la barre oblique inverse est conservé ; tout le reste est supprimé.</span><span class="sxs-lookup"><span data-stu-id="12880-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="12880-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12880-140">Requirements</span></span>



| <span data-ttu-id="12880-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12880-141">Requirement</span></span> | <span data-ttu-id="12880-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="12880-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12880-143">Version</span><span class="sxs-lookup"><span data-stu-id="12880-143">Version</span></span><br/> | <span data-ttu-id="12880-144">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="12880-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="12880-145">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="12880-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="12880-146">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="12880-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="12880-147">DLL</span><span class="sxs-lookup"><span data-stu-id="12880-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="12880-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12880-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="12880-149">IID</span><span class="sxs-lookup"><span data-stu-id="12880-149">IID</span></span><br/>     | <span data-ttu-id="12880-150">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="12880-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="12880-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12880-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12880-152">Correct</span><span class="sxs-lookup"><span data-stu-id="12880-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="12880-153">Types de données de colonne</span><span class="sxs-lookup"><span data-stu-id="12880-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




