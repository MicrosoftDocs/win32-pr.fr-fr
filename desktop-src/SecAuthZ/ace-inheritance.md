---
description: Une liste de contrôle d’accès aux objets peut contenir des ACE qu’elle a héritées de son conteneur parent.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Héritage ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951732"
---
# <a name="ace-inheritance"></a><span data-ttu-id="2b6c1-103">Héritage ACE</span><span class="sxs-lookup"><span data-stu-id="2b6c1-103">ACE Inheritance</span></span>

<span data-ttu-id="2b6c1-104">La liste de contrôle d’accès d’un objet peut contenir des ACE qu’il a hérité de son conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="2b6c1-105">Par exemple, une sous-clé de Registre peut hériter des ACE de la clé située au-dessus de celle-ci dans la hiérarchie du Registre.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="2b6c1-106">De même, un fichier dans un système de fichiers NTFS peut hériter des ACE du répertoire qui le contient.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="2b6c1-107">La structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) d’une entrée du contrôle d’accès contient un jeu d’indicateurs d’héritage qui contrôlent l’héritage ACE et l’effet d’une entrée du contrôle d’accès sur l’objet auquel elle est attachée.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="2b6c1-108">Le système interprète les indicateurs d’héritage et d’autres informations d’héritage en fonction [des règles d’héritage de l’entrée du contrôle d'](ace-inheritance-rules.md)accès.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="2b6c1-109">Ces règles ont été améliorées avec les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b6c1-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="2b6c1-110">Prise en charge de la [propagation automatique des ACE pouvant être héritées](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="2b6c1-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="2b6c1-111">Indicateur qui fait la distinction entre les ACE héritées et les ACE qui ont été directement appliquées à un objet.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="2b6c1-112">Entrées de contrôle d’accès spécifiques aux objets qui vous permettent de spécifier le type d’objet enfant qui peut hériter de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="2b6c1-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="2b6c1-113">La possibilité d’empêcher une liste DACL ou SACL d’hériter des entrées du contrôle d’accès en définissant les \_ \_ bits de \_ contrôle du descripteur DACL protected ou se \_ dans les bits de contrôle [*du descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) , à l’exception de l’attribut de ressource système ACE et de l' \_ ID de \_ \_ \_ stratégie limitée au système \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2b6c1-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
