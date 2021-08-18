---
description: L’action SelfUnregModules annule l’inscription de tous les modules répertoriés dans la table SelfReg qui sont planifiés pour être désinstallés. Le programme d’installation ne s’inscrit pas automatiquement .EXE fichiers.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Action SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ba95a745716d512a72e9541064f56bdc663e2e6c9658a9c35744449217952f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040329"
---
# <a name="selfunregmodules-action"></a>Action SelfUnregModules

L’action SelfUnregModules annule l’inscription de tous les modules répertoriés dans la [table Selfreg](selfreg-table.md) qui sont planifiés pour être désinstallés. Le programme d’installation ne s’inscrit pas automatiquement .EXE fichiers.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit apparaître avant l’action SelfUnregModules dans la séquence. Si une action [SelfRegModules](selfregmodules-action.md) est utilisée, elle doit apparaître après l’action SelfUnregModules dans la séquence. Si une [action RemoveFiles](removefiles-action.md) est utilisée, elle doit apparaître après l’action SelfUnregModules dans la séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                             |
|-------|--------------------------------------------------------|
| \[1\] | Identificateur du fichier de module non inscrit.                |
| \[2\] | Identificateur du dossier contenant le fichier de module non inscrit. |



 

## <a name="remarks"></a>Remarques

L’action SelfUnregModules tente d’appeler la fonction [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) du module dont l’inscription doit être annulée. Cette action s’exécute avec des privilèges élevés lorsque l’installation est exécutée avec des privilèges élevés, par exemple lors d’une installation par ordinateur. Pendant une installation par utilisateur, le programme d’installation exécute cette action avec des privilèges d’utilisateur.

Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation annule l’inscription automatique des dll à l’aide de l’action SelfUnRegModules.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
