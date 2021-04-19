---
title: Notification de données
description: Les objets qui consomment des données provenant d’une source externe doivent parfois être informés lorsque les données de cette source changent.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510498"
---
# <a name="data-notification"></a>Notification de données

Les objets qui consomment des données provenant d’une source externe doivent parfois être informés lorsque les données de cette source changent. Par exemple, une visionneuse de bandes de cotations boursières qui s’appuie sur des données dans une feuille de calcul doit être notifiée lorsque ces données changent afin de pouvoir mettre à jour son affichage. De même, un document composé a besoin d’informations sur les modifications de données dans ses objets incorporés afin qu’il puisse mettre à jour ses caches de données. Dans ce cas, où la mise à jour dynamique des données est souhaitable, les sources de données requièrent un mécanisme de notification des modifications aux consommateurs de données à mesure qu’elles se produisent sans obliger les consommateurs à supprimer tout afin de mettre à jour leurs données. Dans l’idéal, après avoir été informé qu’une modification a eu lieu dans la source de données, un objet consommateur peut demander une copie mise à jour à son gré.

Le mécanisme de COM pour gérer les notifications asynchrones de ce type est un objet appelé récepteur de notifications, qui est tout simplement un objet COM qui implémente une interface appelée [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink). Les consommateurs de données implémentent **IAdviseSink**. Ils s’inscrivent pour recevoir des notifications en transmettant un pointeur vers l’objet de données qui nous intéresse.

Les interfaces [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) exposent les méthodes suivantes pour recevoir des notifications asynchrones :



| Méthode                                                      | Notifie le récepteur de notifications qui                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**N''est**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | Les données de l’objet appelant ont été modifiées.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | Les instructions de dessin de l’objet appelant ont changé.<br/> |
| [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | Le moniker de l’objet appelant a changé.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | L’objet appelant a été enregistré dans un stockage persistant.<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | L’objet appelant a été fermé.<br/>                           |



 

Comme le montre le tableau, l’interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) expose des méthodes pour notifier le récepteur d’événements autres que les modifications apportées aux données de l’objet appelant. L’objet appelant peut également notifier le récepteur lorsque la manière dont il se dessine lui-même change ou qu’il est renommé, enregistré ou fermé. Ces autres notifications sont utilisées principalement ou entièrement dans le contexte des documents composés, bien que le mécanisme de notification soit identique. Pour plus d’informations sur les notifications de documents composés, consultez la section « documents composés ».

Pour tirer parti du récepteur de notifications, une source de données doit implémenter [**IDataObject ::D Advise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject ::D Unadvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)et [**IDataObject :: EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise). Un consommateur de données appelle le mothod **DAdvise** pour notifier un objet de données qu’il souhaite être averti lorsque les données de l’objet sont modifiées. L’objet consommateur appelle la méthode **DUnadvise** pour détruire cette connexion. Toute partie intéressée peut appeler la méthode **EnumDAdvise** pour connaître le nombre d’objets ayant une connexion consultative avec un objet de données.

Lorsque les données sont modifiées au niveau de la source, l’objet de données appelle [**IAdviseSink :: OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) sur tous les consommateurs de données qui se sont inscrits pour recevoir des notifications. Pour effectuer le suivi des connexions de notifications et gérer la distribution des notifications, les sources de données s’appuient sur un objet appelé détenteur de la notification de *données*. Vous pouvez créer votre propre propriétaire de notifications de données en implémentant l’interface [**IDataAdviseHolder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) . Ou vous pouvez laisser COM le faire pour vous en appelant la fonction d’assistance [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de données](data-transfer.md)
</dt> </dl>

 

