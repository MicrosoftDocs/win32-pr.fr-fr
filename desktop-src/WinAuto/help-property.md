---
title: Help, propriété
description: La propriété Help fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6f8b226c483e3a3d68f878fccb940fc1a9f69f18b6fde62eed4b5a7a8ea9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122189"
---
# <a name="help-property"></a>Help, propriété

La propriété **Help** fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.

La propriété **Help** est récupérée en appelant [**IAccessible :: obtenir \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Cette propriété contient des informations de style Balloon (telles qu’elles figurent dans les info-bulles) utilisées pour décrire ce que fait l’objet ou comment l’utiliser. Par exemple, la propriété d' **aide** d’un bouton de barre d’outils qui affiche une imprimante peut fournir le texte suivant : « imprime le document actif ».

Le texte de la propriété **d’aide** n’a pas besoin d’être unique au sein de l’interface utilisateur.

## <a name="when-to-support-the-help-property"></a>Quand prendre en charge la propriété d’aide

Les serveurs ne prennent pas en charge la propriété **d’aide** si d’autres propriétés fournissent des informations suffisantes sur le rôle de l’objet et les actions effectuées par l’objet. Les objets accessibles qui exposent des contrôles fournis par le système ne prennent pas en charge la propriété **Help** .

 

 




