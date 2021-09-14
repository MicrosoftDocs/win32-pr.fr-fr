---
title: Modèle objet du composant OLE
description: Modèle objet du composant OLE
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229830"
---
# <a name="the-ole-component-object-model"></a>Modèle objet du composant OLE

Les objets utilisés par la bibliothèque AVIFile font tous partie du modèle objet du composant OLE. En premier lieu, cela signifie qu’ils partagent certaines méthodes qui les rendent plus faciles à utiliser, et les valeurs qu’elles renvoient sont communes à la plupart des méthodes d’interface OLE.

Le modèle objet composant OLE des gestionnaires de fichiers et de flux utilise l’interface OLE **IClassFactory** pour créer des instances de leur classe d’objet. En tant qu’objets composant, ils implémentent l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , qui se compose des méthodes [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)et [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . L’interface **IUnknown** permet à une application d’obtenir des pointeurs vers d’autres interfaces prises en charge par le même objet.

Vous pouvez déterminer si un objet prend en charge une interface spécifique à l’aide de la méthode **QueryInterface** . Si un objet prend en charge une interface spécifiée, **QueryInterface** retourne un pointeur vers cette interface.

Vous pouvez incrémenter et décrémenter le décompte de références associé à un objet à l’aide des méthodes [**AddRef**](/previous-versions//dd757100(v=vs.85)) et [**Release**](/previous-versions//dd757102(v=vs.85)) . Le nombre de références permet à plusieurs clients d’accéder à un objet. Lorsqu’un objet est utilisé par la première application, son décompte de références a la valeur 1. Les applications utilisent ensuite la méthode **AddRef** pour incrémenter le nombre pour permettre à l’objet d’effectuer le suivi du nombre de fois où il fait l’objet d’un accès.

Quand une application est effectuée à l’aide d’un objet, elle appelle la méthode **Release** pour décrémenter le décompte de références. Lorsque le nombre de références est égal à zéro, l’objet n’est plus nécessaire et libère toutes les ressources qu’il **utilise et détruit** l’objet. Étant donné qu’un objet utilise des ressources internes transparentes pour l’application, l’objet est chargé de les libérer. Par exemple, un gestionnaire de fichiers peut avoir besoin de fermer les fichiers disque ouverts et la mémoire tampon libre lorsqu’ils sont libérés.

La plupart des méthodes d’interface OLE retournent des handles de résultats définis à l’aide du type de données **HRESULT** . Ce type de données est constitué d’un code de gravité, d’informations contextuelles, d’un code d’installation et d’un code d’État. Handle de résultat de retour qui indique que la réussite a la valeur zéro. Une valeur différente de zéro indique un échec et le membre de code d’État du handle de résultat de retour fournit une base pour une interprétation supplémentaire. Pour plus d’informations sur les handles de résultats de retour OLE, consultez le *Guide de référence du programmeur OLE*.

 

 