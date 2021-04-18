---
description: La propriété ProductLanguage spécifie le langage que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propriété ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526786"
---
# <a name="productlanguage-property"></a><span data-ttu-id="76f27-103">Propriété ProductLanguage</span><span class="sxs-lookup"><span data-stu-id="76f27-103">ProductLanguage property</span></span>

<span data-ttu-id="76f27-104">La propriété **ProductLanguage** spécifie le langage que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="76f27-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="76f27-105">Cette propriété doit être un identificateur de langue numérique (LANGID).</span><span class="sxs-lookup"><span data-stu-id="76f27-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="76f27-106">Si une transformation modifie la langue de l’interface utilisateur dans la base de données, elle doit également modifier la valeur de cette propriété pour refléter la nouvelle langue.</span><span class="sxs-lookup"><span data-stu-id="76f27-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="76f27-107">Cette propriété est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76f27-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f27-108">Notes</span><span class="sxs-lookup"><span data-stu-id="76f27-108">Remarks</span></span>

<span data-ttu-id="76f27-109">La valeur de la propriété **ProductLanguage** doit être l’une des langues listées dans la propriété [**Résumé du modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="76f27-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="76f27-110">Lorsque vous créez un package comme indépendant de la langue, affectez la valeur 0 à la propriété **ProductLanguage** et utilisez la police MS Shell Dlg comme style de texte pour toutes les boîtes de dialogue créées.</span><span class="sxs-lookup"><span data-stu-id="76f27-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="76f27-111">Étant donné que certaines polices ne prennent pas en charge tous les jeux de caractères, en utilisant cette police, vous pouvez vous assurer que le texte s’affiche correctement sur toutes les versions localisées du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="76f27-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f27-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76f27-112">Requirements</span></span>



| <span data-ttu-id="76f27-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76f27-113">Requirement</span></span> | <span data-ttu-id="76f27-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="76f27-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f27-115">Version</span><span class="sxs-lookup"><span data-stu-id="76f27-115">Version</span></span><br/> | <span data-ttu-id="76f27-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76f27-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="76f27-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76f27-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="76f27-118">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76f27-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="76f27-119">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="76f27-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76f27-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76f27-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f27-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76f27-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




