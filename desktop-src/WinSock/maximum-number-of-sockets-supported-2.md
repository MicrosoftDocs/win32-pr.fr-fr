---
description: le nombre maximal de sockets pris en charge par un fournisseur de services Windows sockets particulier est spécifique à l’implémentation.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Nombre maximal de sockets pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569750"
---
# <a name="maximum-number-of-sockets-supported"></a>Nombre maximal de sockets pris en charge

le nombre maximal de sockets pris en charge par un fournisseur de services Windows sockets particulier est spécifique à l’implémentation. Le fournisseur Microsoft Winsock limite le nombre maximal de sockets pris en charge uniquement par la mémoire disponible sur l’ordinateur local. Toutefois, les fournisseurs Winsock tiers peuvent avoir des limitations sur le nombre de sockets pris en charge. Une application ne doit pas faire d’hypothèses sur la disponibilité d’un certain nombre de Sockets. Pour plus d’informations sur cette rubrique, consultez [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ set et SELECT

un certain nombre de \_ macros FD XXX sont définies dans le fichier d’en-tête *Winsock2. h* pour une utilisation dans le portage des applications afin de Windows à partir de l’environnement UNIX. Ces macros sont utilisées avec les fonctions [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) et [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) pour le portage des applications à Windows. le nombre maximal de sockets qu’une application de Windows sockets peut utiliser n’est pas affecté par la constante de manifeste FD \_ . Cette valeur définie dans le fichier d’en-tête *Winsock2. h* est utilisée lors de la construction des structures [**FD \_ Set**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilisées avec la fonction **Select** . La valeur par défaut dans Winsock2. h est 64. Si une application est conçue pour pouvoir travailler avec plus de 64 sockets à l’aide des fonctions **Select** et **WSAPoll** , l’implémenteur doit définir la fonction FD \_ de manifeste dans chaque fichier source avant d’inclure le fichier d’en-tête *Winsock2. h* . L’une des méthodes possibles consiste à inclure la définition dans les options du compilateur dans le Makefile. Par exemple, vous pouvez ajouter « -DFD \_ deinstall = 128 » comme option à la ligne de commande du compilateur pour Microsoft C++. il faut insister sur le fait que \_ la définition de FD configure en tant que valeur particulière n’a aucun effet sur le nombre réel de sockets fournis par un fournisseur de service de sockets Windows. Cette valeur affecte uniquement les \_ macros FD xxx utilisées par les fonctions **Select** et **WSAPoll** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ensemble FD**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sélectionné**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
