---
description: Les noms DNS se composent d’un ou plusieurs composants séparés par un point (par exemple, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Noms d'ordinateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf076f42e3353aa03db951e9dec428766cf4895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869226"
---
# <a name="computer-names"></a>Noms d'ordinateur

Les noms DNS se composent d’un ou plusieurs composants séparés par un point (par exemple, msdn.microsoft.com). Chaque composant peut comporter jusqu’à 63 octets. Chaque nom peut comporter jusqu’à 255 octets au total. Les noms DNS sont représentés dans le jeu de caractères UTF-8 ou Unicode. Ce nom ne respecte pas la casse. Pour plus d’informations, consultez [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Un ordinateur est identifié de manière unique par son nom DNS complet, qui se compose de son nom d’hôte DNS et du nom du domaine DNS auquel il est attribué. Pour récupérer le nom DNS complet d’un ordinateur, le nom d’hôte DNS ou le nom de domaine DNS, appelez la fonction [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) . Pour définir le nom d’hôte DNS ou le nom de domaine DNS d’un ordinateur, appelez la fonction [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) . Les modifications de nom ne prennent pas effet tant que l’utilisateur n’a pas redémarré l’ordinateur.

Les noms NetBIOS comportent jusqu’à 15 octets de caractères OEM, notamment des lettres, des chiffres, des traits d’Union et des points. Certains caractères sont spécifiques au jeu de caractères. Les noms NetBIOS sont généralement représentés dans le jeu de caractères OEM. Le jeu de caractères OEM dépend des paramètres régionaux. Certains jeux de caractères OEM représentent certains caractères sous la forme de deux octets. Les noms NetBIOS, par Convention, sont représentés en majuscules lorsque l’algorithme de traduction des minuscules et majuscules est dépendant du jeu de caractères OEM.

Les fonctions [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) et [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) peuvent également définir et récupérer le nom NetBIOS de l’ordinateur. Par Convention, le nom NetBIOS et le nom d’hôte DNS sont interdépendants. Lorsque vous modifiez le nom DNS, le nom NetBIOS est également mis à jour. Le nom NetBIOS est la représentation OEM du nom d’hôte DNS jusqu’à la \_ longueur maximale des \_ caractères ComputerName. Si vous définissez un nom d’hôte DNS supérieur à la longueur maximale du nom d' \_ ordinateur \_ , le nom NetBIOS est défini sur une version tronquée du nom d’hôte DNS. Dans le cas contraire, le nom d’hôte DNS entier est converti en nom NetBIOS OEM. AVERTISSEMENT : Si vous modifiez le nom NetBIOS afin qu’il ne s’agit pas d’un mappage tronqué du nom DNS, vous allez rompre les applications qui utilisent des fonctions telles que [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) qui reposent sur cette Convention.

 

 
