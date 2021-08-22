---
description: Wmiadap est une application qui s’exécute sur Windows qui peut mettre à jour les informations de performances dans l’espace de stockage WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a58de2ca5e678cbbb99f803415572be236f2a545ed149b9ad598fb7f9a4664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049837"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap est une application qui s’exécute sur Windows qui peut mettre à jour les informations de performances dans l’espace de stockage WMI. En général, cela permet aux développeurs et aux administrateurs informatiques de créer des scripts qui accèdent aux informations sur les performances, telles que la quantité de mémoire utilisée par une application. La rubrique suivante décrit l’interface de ligne de commande que vous pouvez utiliser pour contrôler la façon dont wmiadap récupère les informations.

Wmiadap est installé avec le système d’exploitation sur la plupart des systèmes, dans le répertoire C : \\ Windows \\ System32 \\ wbem. Si vous constatez des messages d’erreur concernant wmiadap.exe, recherchez [support Microsoft](https://support.microsoft.com/). En règle générale, vous ne devez pas supprimer wmiadap.exe de votre système, sauf instruction contraire.

Le transfert de données à partir des bibliothèques de performance et l’actualisation des classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) sont effectués par les fournisseurs [WmiPerfClass](wmi-providers.md) et [wmiperfinst](wmi-providers.md) . Le fournisseur WmiPerfClass met à jour les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI uniquement lorsqu’un nouvel objet de performance est ajouté. vous pouvez toujours exécuter Wmiadap avec le commutateur **/r** pour analyser les pilotes Windows Driver Model afin de créer des objets de performance. Le commutateur **/f** force toujours une mise à jour des classes WMI à partir des bibliothèques de performances.

Les commutateurs suivants sont disponibles à l’invite de commandes.

**wmiadap** \[  \] /f \[ **/r**\]

## <a name="switches"></a>Commutateurs

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analyse toutes les bibliothèques de performances du système et actualise les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

analyse tous les pilotes Windows Driver Model sur le système pour créer des objets de performance.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**critique**](winmgmt.md)
</dt> </dl>

 

 
