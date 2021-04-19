---
description: L’action SelfRegModules traite tous les modules listés dans la table SelfReg et inscrit tous les modules installés sur le système. Le programme d’installation n’enregistre pas automatiquement les fichiers EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Action SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535040"
---
# <a name="selfregmodules-action"></a>Action SelfRegModules

L’action SelfRegModules traite tous les modules listés dans la table [Selfreg](selfreg-table.md) et inscrit tous les modules installés sur le système. Le programme d’installation n’enregistre pas automatiquement les fichiers EXE.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler l’action SelfRegModules. Si une action [InstallFiles](installfiles-action.md) est utilisée, elle doit apparaître avant l’action SelfRegModules dans la séquence. Étant donné que l’action SelfRegModules change le système, SelfRegModules doit venir après l' [action InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                           |
|-------|------------------------------------------------------|
| \[1\] | Identificateur du fichier de module inscrit.                |
| \[2\] | Identificateur du dossier contenant le fichier de module inscrit. |



 

## <a name="remarks"></a>Notes

L’action SelfRegModules tente d’appeler la fonction [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) du module planifié pour être inscrit. Cette action s’exécute avec des privilèges élevés lorsque l’installation est exécutée avec des privilèges élevés, par exemple lors d’une installation par ordinateur. Au cours d’une installation par utilisateur, le programme d’installation exécute cette action avec des privilèges d’utilisateur.

Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation inscrit des dll à inscription automatique à l’aide de l' [action SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
