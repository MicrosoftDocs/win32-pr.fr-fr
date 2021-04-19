---
description: Le registre système contient les données de configuration utilisées par le système d’exploitation, les services et les applications.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modification du Registre système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515808"
---
# <a name="modifying-the-system-registry"></a>Modification du Registre système

Le registre système contient les données de configuration utilisées par le système d’exploitation, les services et les applications. Windows Management Instrumentation (WMI) a un [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) et la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) avec des méthodes qui permettent d’analyser ou de modifier le registre sur l’ordinateur local ou les ordinateurs distants. Le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider) prend en charge la classe de [**\_ Registre Win32**](/windows/desktop/CIMWin32Prov/win32-registry) qui contient des données statiques relatives à la taille d’un registre.

Le fournisseur de Registre système est une instance, une propriété et un fournisseur d’événements qui s’interface avec le registre système. Le fournisseur de Registre système est un fournisseur standard avec l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Vous pouvez utiliser le fournisseur de Registre système pour accéder aux clés de Registre et aux informations sur les systèmes locaux et distants. Pour plus d’informations, consultez [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI place le [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) dans l' \\ espace de noms racine par défaut. Toutefois, vous pouvez compiler le fichier Regevent. mof dans d’autres espaces de noms à utiliser par d’autres applications.

Les rubriques identifiées dans le tableau suivant peuvent vous montrer comment utiliser la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) et le fournisseur de Registre système.



| Rubrique                                                                                              | Description                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtention de données de Registre](obtaining-registry-data.md)                                             | Vous pouvez obtenir ou modifier les données du Registre par le biais de méthodes de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) , ce qui vous permet d’automatiser les activités du Registre localement ou à distance.                    |
| [Modification des données de Registre](changing-registry-data.md)                                               | Vous pouvez ajouter ou supprimer des clés, et ajouter ou modifier des valeurs d’entrée de Registre sous clés.                                                                                                                    |
| [Programmation avec le fournisseur de Registre système](programming-with-the-system-registry-provider.md) | Vous pouvez définir vos propres classes fournies par le registre système avec des données.                                                                                                                       |
| [Inscription pour les événements du Registre système](registering-for-system-registry-events.md)               | Le fournisseur de Registre système peut envoyer des événements à un consommateur. Pour recevoir des événements, vous devez inscrire votre consommateur, créer une requête, puis vous assurer que le fournisseur vous envoie correctement les événements. |
| [Inscription du fournisseur de Registre système](registering-the-system-registry-provider.md)           | Le fournisseur Registre système est inscrit dans le cadre du processus d’installation de WMI.                                                                                                                |



 

 

 
