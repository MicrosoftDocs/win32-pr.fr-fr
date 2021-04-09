---
title: Entrées de Registre (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'En savoir plus sur : entrées de Registre (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111454"
---
# <a name="registry-entries-com"></a>Entrées de Registre (COM)

Les valeurs de Registre dans les clés de Registre suivantes contrôlent les aspects de la fonctionnalité de COM :

-   [**HKEY \_ local \_ machine \\ classes de logiciels \\**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

À compter de Windows Server 2003, COM utilise uniquement le jeton de processus actuel pour décider de la ruche de Registre à laquelle accéder, et non le jeton de thread. Si COM n’est pas en mesure d’accéder à la ruche du Registre du profil utilisateur, il accède à la ruche du système de l' **\_ \_ ordinateur \\ local HKEY** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registre](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
