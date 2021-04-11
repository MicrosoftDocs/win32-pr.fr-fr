---
title: Objet de police standard
description: Objet de police standard
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031894"
---
# <a name="standard-font-object"></a>Objet de police standard

La propriété de police ambiante standard fournie par le conteneur et la propriété de police standard fournie par le contrôle fournissent toutes deux un objet de police standard. Autrement dit, ces polices standard fournissent un pointeur **IDispatch** vers un objet de police standard.

L’objet font est une implémentation fournie par le système d’un ensemble d’interfaces par-dessus la prise en charge des polices GDI sous-jacentes. Un objet de police est créé via la fonction API [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) à partir d’une structure [**fontdesc**](/windows/win32/api/olectl/ns-olectl-fontdesc) . L’objet font prend en charge plusieurs propriétés de lecture/écriture, ainsi que des méthodes personnalisées via son [**IFont interface IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont), et prend en charge le même jeu de propriétés (mais pas les méthodes) via une [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)dispinterface. La dispinterface est utilisée pour les propriétés de police mentionnées précédemment. Les propriétés correspondent aux attributs de police GDI qui sont décrits dans la structure [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) .

L’objet font prend également en charge l' [**interface de**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) l’interface de sortie, qui permet à un client de déterminer quand les propriétés de police changent. Étant donné que l’objet font prend en charge au moins une interface sortante, il implémente également [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) et un point de connexion pour **IPropertyNotifySink** à cet effet.

L’objet font fournit une propriété hFont qui est un handle de police Windows conforme aux autres attributs spécifiés pour la police. L’objet font retarde la réalisation de cette police dans la mesure du possible. par conséquent, la définition consécutive de deux propriétés sur une police n’entraîne pas la mise en place d’une police intermédiaire. En outre, en tant qu’optimisation, l’objet de police standard gère un cache de poignées de police. Deux objets de police dans le même processus qui ont des propriétés identiques retournent le même descripteur de police. L’objet de police peut supprimer des polices de ce cache à la place, ce qui présente des considérations spéciales pour les clients qui utilisent cette propriété hFont. Pour plus d’informations, consultez [**IFont :: obtenir \_ Hfont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) .

L’objet de police prend également en charge [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , de sorte qu’il peut s’enregistrer et se charger à partir d’une instance de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Tout autre objet qui utilise un objet font en interne enregistre et charge la police dans le cadre de la gestion de la persistance de l’objet.

En outre, l’objet font prend en charge [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) par le biais duquel il fournit un jeu de propriétés contenant des valeurs typées pour chaque propriété font.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle](control-properties.md)
</dt> </dl>

 

 