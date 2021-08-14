---
title: Implémentation de l’objet COM du menu contextuel
description: Une extension de menu contextuel est un objet COM implémenté en tant que serveur in-proc.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- objet COM du menu contextuel AD
- objet COM du menu contextuel AD, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac371ea64239c18de2a8f30c969eb6d920221f0a802f18ceeebfef2c3991e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187647"
---
# <a name="implementing-the-context-menu-com-object"></a>Implémentation de l’objet COM du menu contextuel

Une extension de menu contextuel est un objet COM implémenté en tant que serveur in-proc. L’extension du menu contextuel doit implémenter les interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Une extension de menu contextuel est instanciée lorsque l’utilisateur affiche le menu contextuel d’un objet d’une classe pour laquelle l’extension de menu contextuel a été inscrite.

## <a name="implementing-ishellextinit"></a>Implémentation de IShellExtInit

Après l’instanciation de l’objet COM de l’extension de menu contextuel, la méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) est appelée. **IShellExtInit :: Initialize** fournit l’extension de menu contextuel avec un objet [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) qui contient les données pertinentes pour l’objet d’annuaire auquel le menu contextuel s’applique.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contient des données au format [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Le format de données **CFSTR \_ DSOBJECTNAMES** est un **HGLOBAL** qui contient une structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La structure **DSOBJECTNAMES** contient des données sur l’objet Directory auquel s’applique l’extension de la feuille de propriétés.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contient également des données au format [**CFSTR \_ DS \_ Display \_ spec \_ options**](cfstr-ds-display-spec-options.md) . Le format de données **CFSTR \_ DS \_ Display \_ spec \_ options** est un **HGLOBAL** qui contient une structure [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . Le **DSDISPLAYSPECOPTIONS** contient des données de configuration utilisables par l’extension.

Si une valeur autre que **S \_ OK** est retournée à partir de [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), l’extension du menu contextuel ne sera pas utilisée.

Les paramètres *pidlFolder* et *hkeyProgID* de la méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) ne sont pas utilisés.

## <a name="implementing-icontextmenu"></a>Implémentation de IContextMenu

Après que [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) retourne, la méthode [**IContextMenu :: QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) est appelée pour obtenir l’élément de menu ou les éléments que l’extension de menu contextuel ajoutera. L’implémentation de **QueryContextMenu** est relativement simple. L’extension du menu contextuel ajoute ses éléments de menu à l’aide de la fonction [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ou similaire. Les identificateurs de commandes de menu doivent être supérieurs ou égaux à *idCmdFirst* et doivent être inférieurs à *idCmdLast*. **QueryContextMenu** doit retourner le plus grand identificateur numérique ajouté au menu plus un. La meilleure façon d’affecter des identificateurs de commandes de menu consiste à commencer à zéro et à travailler en séquence. Si l’extension du menu contextuel n’a besoin d’aucun élément de menu, elle ne doit tout simplement pas ajouter d’éléments au menu et retourner zéro à partir de **QueryContextMenu**.

[**IContextMenu :: GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) est appelé pour extraire des données textuelles pour l’élément de menu, telles que le texte d’aide à afficher pour l’élément de menu. Il est possible que l’hôte de menu contextuel utilise des chaînes Unicode alors que l’extension utilise des chaînes ANSI. Pour cette raison, les **cas \_ GC HELPTEXTA**, **GC \_ HELPTEXTW**, **GC \_ Verba** et **GC \_ VERBW** doivent être traités individuellement. L’implémentation de cette méthode est facultative.

[**IContextMenu :: commande InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé quand l’un des éléments de menu installés par l’extension de menu contextuel est sélectionné. Le menu contextuel exécute ou initie les actions souhaitées en réponse à cette méthode.

 

 