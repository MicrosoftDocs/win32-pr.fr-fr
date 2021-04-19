---
description: La méthode RegistryValue de l’objet installer lit les informations relatives à une clé de Registre spécifiée de valeur.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. RegistryValue, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543205"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="1a6fc-103">Installer. RegistryValue, méthode</span><span class="sxs-lookup"><span data-stu-id="1a6fc-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="1a6fc-104">La méthode **RegistryValue** de l’objet [**installer**](installer-object.md) lit les informations relatives à une clé de Registre spécifiée de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="1a6fc-105">Si la clé ou la valeur spécifiée n’existe pas, la méthode retourne une erreur 9, « indice hors limites ».</span><span class="sxs-lookup"><span data-stu-id="1a6fc-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a6fc-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="1a6fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a6fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6fc-108">*root*</span><span class="sxs-lookup"><span data-stu-id="1a6fc-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6fc-109">Dans Windows NT 4,0, la racine du Registre est soit une clé racine numérique, soit un nom d’ordinateur en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="1a6fc-110">Les noms d’ordinateur sont toujours des chaînes.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-110">Machine names are always strings.</span></span> <span data-ttu-id="1a6fc-111">Dans Windows 95, Windows 98 ou Windows Me, la racine du Registre est une clé racine numérique uniquement.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="1a6fc-112">Vous pouvez uniquement accéder à HKLM sur une machine distante.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="1a6fc-113">Root</span><span class="sxs-lookup"><span data-stu-id="1a6fc-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="1a6fc-114">Signification</span><span class="sxs-lookup"><span data-stu-id="1a6fc-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="1a6fc-115"><dt>**\_racine des classes HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="1a6fc-116">0</span><span class="sxs-lookup"><span data-stu-id="1a6fc-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="1a6fc-117"><dt>**HKEY \_ Current \_ User**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="1a6fc-118">1</span><span class="sxs-lookup"><span data-stu-id="1a6fc-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="1a6fc-119"><dt>**HKEY \_ local \_ machine**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="1a6fc-120">2</span><span class="sxs-lookup"><span data-stu-id="1a6fc-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="1a6fc-121"><dt>**HKEY, \_ utilisateurs**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="1a6fc-122">3</span><span class="sxs-lookup"><span data-stu-id="1a6fc-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="1a6fc-123"><dt>**\_données de performances HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="1a6fc-124">4</span><span class="sxs-lookup"><span data-stu-id="1a6fc-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="1a6fc-125"><dt>**configuration de HKEY \_ Current \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="1a6fc-126">5</span><span class="sxs-lookup"><span data-stu-id="1a6fc-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="1a6fc-127"><dt>**\_données HKEY dyn \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="1a6fc-128">6</span><span class="sxs-lookup"><span data-stu-id="1a6fc-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1a6fc-129">*key*</span><span class="sxs-lookup"><span data-stu-id="1a6fc-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6fc-130">Chaîne contenant le chemin d’accès complet à la clé à partir de la racine.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="1a6fc-131">*value*</span><span class="sxs-lookup"><span data-stu-id="1a6fc-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6fc-132">Ce paramètre facultatif désigne la valeur associée à retourner pour la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="1a6fc-133">La valeur est l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="1a6fc-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a6fc-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="1a6fc-135">Signification</span><span class="sxs-lookup"><span data-stu-id="1a6fc-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="1a6fc-136"><dt>**Manquant ou vide**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="1a6fc-137">Retourne une valeur booléenne désignant si la clé existe.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="1a6fc-138"><dt>**String**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="1a6fc-139">Retourne les données associées à la valeur nommée, échoue si le nom de la valeur n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="1a6fc-140"><dt>**Entier positif**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="1a6fc-141">Retourne le nom de la valeur énumérée de base 1, il est vide s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="1a6fc-142">Cette option utilise la fonction [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .</span><span class="sxs-lookup"><span data-stu-id="1a6fc-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="1a6fc-143"><dt>**Entier négatif**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="1a6fc-144">Retourne le nom de la sous-clé énumérée de base 1, ce qui est vide s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="1a6fc-145">Cette option utilise la fonction [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .</span><span class="sxs-lookup"><span data-stu-id="1a6fc-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="1a6fc-146"><dt>**Entier zéro**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="1a6fc-147">Retourne le nom de la classe de chaîne pour la clé désignée.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="1a6fc-148"><dt>**Chaîne vide ""**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="1a6fc-149">Retourne la valeur par défaut de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6fc-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a6fc-150">Return value</span></span>

<span data-ttu-id="1a6fc-151">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6fc-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a6fc-152">Requirements</span></span>



| <span data-ttu-id="1a6fc-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a6fc-153">Requirement</span></span> | <span data-ttu-id="1a6fc-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a6fc-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6fc-155">Version</span><span class="sxs-lookup"><span data-stu-id="1a6fc-155">Version</span></span><br/> | <span data-ttu-id="1a6fc-156">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1a6fc-157">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a6fc-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1a6fc-158">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a6fc-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1a6fc-159">DLL</span><span class="sxs-lookup"><span data-stu-id="1a6fc-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a6fc-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6fc-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1a6fc-161">IID</span><span class="sxs-lookup"><span data-stu-id="1a6fc-161">IID</span></span><br/>     | <span data-ttu-id="1a6fc-162">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1a6fc-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
