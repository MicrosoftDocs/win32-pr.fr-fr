---
description: Chaque canal nommé a un nom unique qui le distingue des autres canaux nommés de la liste des systèmes des objets nommés. Un serveur de canaux spécifie un nom pour le canal lorsqu’il appelle la fonction CreateNamedPipe pour créer une ou plusieurs instances d’un canal nommé.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Noms de canaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545076"
---
# <a name="pipe-names"></a>Noms de canaux

Chaque canal nommé a un nom unique qui le distingue des autres canaux nommés dans la liste des objets nommés du système. Un serveur de canaux spécifie un nom pour le canal lorsqu’il appelle la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) pour créer une ou plusieurs instances d’un canal nommé. Les clients de canal spécifient le nom du canal lorsqu’ils appellent la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) pour se connecter à une instance du canal nommé.

Utilisez la forme suivante quand vous spécifiez le nom d’un canal dans la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :

\\\\*Nom du serveur* \\ canal \\ *PipeName*

où *ServerName* est le nom d’un ordinateur distant ou d’un point, pour spécifier l’ordinateur local. La chaîne de nom de canal spécifiée par *PipeName* peut inclure n’importe quel caractère autre qu’une barre oblique inverse, y compris des chiffres et des caractères spéciaux. La chaîne du nom de canal entier peut comporter jusqu’à 256 caractères. Les noms de canaux ne respectent pas la casse.

Le serveur de canal ne peut pas créer un canal sur un autre ordinateur, donc [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) doit utiliser un point pour le nom du serveur, comme illustré dans l’exemple suivant.

\\\\.\\ canal \\ *PipeName*

Un serveur de canaux peut fournir le nom du canal à ses clients de canal, afin qu’ils puissent se connecter au canal. Le client de canal Découvre le nom du canal à partir d’une source persistante, telle qu’une entrée de Registre, un fichier ou une autre application. Dans le cas contraire, les clients doivent connaître le nom du canal au moment de la compilation.

 

 
