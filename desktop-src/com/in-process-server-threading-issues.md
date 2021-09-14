---
title: Problèmes liés aux threads In-Process Server
description: Problèmes liés aux threads In-Process Server
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998911"
---
# <a name="in-process-server-threading-issues"></a>Problèmes liés aux threads In-Process Server

Un serveur in-process n’appelle pas [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)ou [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) pour marquer son modèle de thread. Pour les objets DLL ou in-process prenant en compte les threads, vous devez définir le modèle de thread dans le registre. Le modèle par défaut quand vous ne spécifiez pas de modèle de thread est un thread unique par processus. Pour spécifier un modèle, vous ajoutez la valeur **ThreadingModel** à la clé [InprocServer32](inprocserver32.md) dans le registre.

Les dll qui prennent en charge l’instanciation d’un objet de classe doivent implémenter et exporter les fonctions [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) et [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow). Lorsqu’un client souhaite une instance de la classe prise en charge par la DLL, un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (directement ou via un appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) appelle **DllGetClassObject** pour obtenir un pointeur vers son objet de classe lorsque l’objet est implémenté dans une dll. **DllGetClassObject** devrait donc pouvoir attribuer plusieurs objets de classe ou un seul objet thread-safe (essentiellement en utilisant [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) sur leurs décomptes de références internes).

Comme son nom l’indique, [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) est appelé pour déterminer si la dll qui l’implémente est en cours d’utilisation, ce qui permet à l’appelant de le décharger en toute sécurité si ce n’est pas le cas. Les appels à [**coFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) à partir de n’importe quel thread sont toujours acheminés via le thread du cloisonnement principal pour appeler **DllCanUnloadNow**.

Comme les autres serveurs, les serveurs in-process peuvent être à thread unique, à thread cloisonné ou à thread libre. Ces serveurs peuvent être utilisés par n’importe quel client OLE, quel que soit le modèle de thread utilisé par ce client.

Toutes les combinaisons d’interopérabilité de modèle de thread sont autorisées entre les clients et les objets in-process. L’interaction entre un client et un objet in-process qui utilise différents modèles de threads est identique à l’interaction entre les clients et les serveurs hors processus. Pour un serveur in-process, lorsque le modèle de thread du client et du serveur in-process diffère, COM doit s’interposer entre le client et l’objet.

Lorsqu’un objet in-process qui prend en charge le modèle à thread unique est appelé simultanément par plusieurs threads d’un client, COM ne peut pas autoriser les threads clients à accéder directement à l’interface de l’objet. l’objet n’a pas été conçu pour ce type d’accès. Au lieu de cela, COM doit s’assurer que les appels sont synchronisés et sont effectués uniquement par le thread client qui a créé l’objet. Par conséquent, COM crée l’objet dans le cloisonnement principal du client et nécessite que tous les autres Apartments (cloisonnés) clients accèdent à l’objet à l’aide de proxys.

Lorsqu’un cloisonnement à threads libres (modèle multithread cloisonné) dans un client crée un serveur in-process thread cloisonné, COM lance un thread « hôte » de modèle de cloisonnement monothread dans le client. Ce thread hôte crée l’objet et le pointeur d’interface est remarshalé vers le cloisonnement libre de thread du client. De même, lorsqu’un cloisonnement monothread dans un client de modèle cloisonné crée un serveur in-process libre de threads, COM lance un thread hôte libre de threads (cloisonnement multithread sur lequel l’objet sera créé, puis remarshalé vers le cloisonnement du client à thread unique cloisonné).

> [!Note]  
> En général, si vous concevez une interface personnalisée sur un serveur in-process, vous devez également fournir le code de marshaling pour celle-ci afin que COM puisse marshaler l’interface entre les cloisonnements client.

 

COM vous aide à protéger l’accès aux objets fournis par une DLL à thread unique en exigeant l’accès à partir du cloisonnement du client dans lequel ils ont été créés. En outre, tous les points d’entrée de DLL (tels que [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) et [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) et les données globales doivent toujours être accessibles par le même cloisonnement. COM crée de tels objets dans le cloisonnement principal du client, ce qui donne au principal un accès direct aux pointeurs de l’objet. Les appels des autres cloisonnements utilisent le marshaling entre threads pour passer du proxy au stub dans le cloisonnement principal, puis à l’objet. Cela permet à COM de synchroniser les appels à l’objet. Les appels entre les threads étant lents, il est recommandé de réécrire ces serveurs pour prendre en charge plusieurs cloisonnements.

Comme un serveur in-process à thread unique, un objet fourni par une DLL de modèle cloisonné doit être accessible par le même cloisonnement client à partir duquel il a été créé. Toutefois, les objets fournis par ce serveur peuvent être créés dans plusieurs Apartments du client, de sorte que le serveur doit implémenter ses points d’entrée (tels que [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) et [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) pour une utilisation multithread. Par exemple, si deux cloisonnements d’un client essaient de créer simultanément deux instances de l’objet in-process, **DllGetClassObject** peut être appelé simultanément par les deux cloisonnements. **DllCanUnloadNow** doit être écrit de sorte que la dll ne se décharge pas pendant que le code est toujours en cours d’exécution dans la dll.

Si la DLL fournit une seule instance de la fabrique de classe pour créer tous les objets, l’implémentation de la fabrique de classe doit également être conçue pour une utilisation multithread, car elle est accessible par plusieurs Apartments (cloisonnés) clients. Si la DLL crée une nouvelle instance de la fabrique de classes à chaque fois que [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) est appelé, la fabrique de classe n’a pas besoin d’être thread-safe.

Les objets créés par la fabrique de classe n’ont pas besoin d’être thread-safe. Une fois créé par un thread, l’objet est toujours accessible par le biais de ce thread et tous les appels à l’objet sont synchronisés par COM. Le cloisonnement de modèle Apartment d’un client qui crée cet objet obtiendra un pointeur direct vers l’objet. Les Apartments client qui diffèrent du cloisonnement dans lequel l’objet a été créé doivent accéder à l’objet par le biais de proxies. Ces proxies sont créés lorsque le client marshale l’interface entre ses Apartments.

Quand une valeur **ThreadingModel** de dll in-process est définie sur « both », un objet fourni par cette dll peut être créé et utilisé directement (sans proxy) dans des cloisonnements de clients monothread ou multithread. Toutefois, il ne peut être utilisé directement que dans le cloisonnement dans lequel il a été créé. Pour attribuer l’objet à un autre cloisonnement, l’objet doit être marshalé. L’objet DLL doit implémenter sa propre synchronisation et il est accessible par plusieurs cloisonnements client en même temps.

Pour accélérer les performances de l’accès en thread libre aux objets DLL in-process, COM fournit la fonction [**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) . Cette fonction crée un objet de marshaling libre de threads qui peut être agrégé avec un objet serveur in-process. Lorsqu’un cloisonnement client dans le même processus a besoin d’accéder à un objet dans un autre cloisonnement, l’agrégation du marshaleur libre-thread fournit au client un pointeur direct vers l’objet serveur, plutôt que vers un proxy, lorsque le client marshale l’interface de l’objet vers un autre cloisonnement. Le client n’a pas besoin d’effectuer de synchronisation. Cela fonctionne uniquement dans le même processus. le marshaling standard est utilisé pour une référence à l’objet qui est envoyé à un autre processus.

Un objet fourni par une DLL in-process qui prend uniquement en charge le Threading libre est un objet à thread libre. Il implémente sa propre synchronisation et est accessible par plusieurs threads clients en même temps. Ce serveur ne marshale pas les interfaces entre les threads. ce serveur peut donc être créé et utilisé directement (sans proxy) uniquement par des Apartments multithread dans un client. Les Apartments à thread unique qui le créent y accèdent via un proxy.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Choix du modèle de thread](choosing-the-threading-model.md)
</dt> <dt>

[Apartments (cloisonnés) multithread](multithreaded-apartments.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
</dt> </dl>

 

 