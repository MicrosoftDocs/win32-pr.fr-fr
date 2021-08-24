---
Description: 'Les options de protection de la mémoire sont les suivantes : vous devez spécifier l’une des valeurs suivantes lors de l’allocation ou de la protection d’une page en mémoire. Les attributs de protection ne peuvent pas être assignés à une partie d’une page ; elles ne peuvent être affectées qu’à une page entière.'
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Constantes de protection mémoire (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 187e8e1f4e137823451771309c9cce19db2e7fbd9c5b57597b51cfc58ca61297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067689"
---
# <a name="memory-protection-constants"></a>Constantes de protection de la mémoire

Les options de protection de la mémoire sont les suivantes : vous devez spécifier l’une des valeurs suivantes lors de l’allocation ou de la protection d’une page en mémoire. Les attributs de protection ne peuvent pas être assignés à une partie d’une page ; elles ne peuvent être affectées qu’à une page entière.

## <a name="example"></a>Exemples

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
par exemple, il s’agit d' [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) sur GitHub.

## <a name="constants"></a>Constantes


| Constante/valeur                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**Page \_ EXÉCUTER**</dt> <dt>0x10</dt> </dl>                                       | Active l’accès en exécution à la région de pages validée. Toute tentative d’écriture dans la région validée entraîne une violation d’accès.<br/> Cet indicateur n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**Page \_ EXÉCUTER la \_ lecture**</dt> <dt>0x20</dt> </dl>                       | Active l’accès en lecture ou en lecture seule à la région validée de pages. Toute tentative d’écriture dans la région validée entraîne une violation d’accès.<br/> **Windows Server 2003 et Windows XP :** cet attribut n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) tant que Windows XP avec SP2 et Windows Server 2003 avec SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**Page \_ EXECUTe \_ ReadWrite**</dt> <dt>0x40</dt> </dl>        | Active l’accès en lecture, en lecture seule ou en lecture/écriture à la région de pages validées.<br/> **Windows Server 2003 et Windows XP :** cet attribut n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) tant que Windows XP avec SP2 et Windows Server 2003 avec SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**Page \_ EXÉCUTER \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Active l’accès en lecture, en lecture seule ou en copie sur écriture à une vue mappée d’un objet de mappage de fichier. Toute tentative d’écriture dans une page de copie sur écriture validée entraîne la mise en œuvre d’une copie privée de la page pour le processus. La page privée est marquée en tant que **page \_ Execute \_ ReadWrite**, et la modification est écrite dans la nouvelle page.<br/> Cet indicateur n’est pas pris en charge par les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) . **Windows Vista, Windows Server 2003 et Windows XP :** cet attribut n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) tant que Windows Vista avec SP1 et Windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**Page \_ NoAccess**</dt> <dt>0x01</dt> </dl>                                    | Désactive tout accès à la région de pages validée. Une tentative de lecture, d’écriture ou d’exécution de la région validée entraîne une violation d’accès.<br/> Cet indicateur n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**Page \_ READONLY**</dt> <dt>0x02</dt> </dl>                                    | Active l’accès en lecture seule à la région validée des pages. Toute tentative d’écriture dans la région validée entraîne une violation d’accès. Si la [prévention de l’exécution des données](data-execution-prevention.md) est activée, une tentative d’exécution du code dans la région validée entraîne une violation d’accès.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**Page \_ READWRITE**</dt> <dt>0x04</dt> </dl>                                 | Active l’accès en lecture seule ou en lecture/écriture à la région validée des pages. Si la [prévention de l’exécution des données](data-execution-prevention.md) est activée, toute tentative d’exécution du code dans la région engagée entraîne une violation d’accès.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**Page \_ WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Active l’accès en lecture seule ou en copie sur écriture à une vue mappée d’un objet de mappage de fichier. Toute tentative d’écriture dans une page de copie sur écriture validée entraîne la mise en œuvre d’une copie privée de la page pour le processus. La page privée est marquée comme **page \_ ReadWrite** et la modification est écrite dans la nouvelle page. Si la [prévention de l’exécution des données](data-execution-prevention.md) est activée, toute tentative d’exécution du code dans la région engagée entraîne une violation d’accès.<br/> Cet indicateur n’est pas pris en charge par les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**Page \_ CIBLE les 0x40000000 \_ non valides**</dt> <dt></dt> </dl>        | Définit tous les emplacements des pages en tant que cibles non valides pour CFG. Utilisé avec n’importe quelle protection de page d’exécution comme **page \_ Execute**, **page \_ Execute \_ Read**, **page \_ Execute \_ ReadWrite** et **page \_ Execute \_ WRITECOPY**. Tout appel indirect aux emplacements de ces pages entraînera l’échec des vérifications de CFG et le processus sera terminé. Le comportement par défaut pour les pages exécutables allouées doit être marqué comme cibles d’appel valides pour CFG.<br/> Cet indicateur n’est pas pris en charge par les fonctions [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) ou [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**Page \_ CIBLES \_ sans 0x40000000 de \_ mise à jour**</dt> <dt></dt> </dl> | Les informations CFG des pages de la région ne seront pas mises à jour pendant la modification de la protection de [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect). Par exemple, si les pages de la région ont été allouées à l’aide de **cibles de page \_ \_ non valides**, les informations non valides sont conservées pendant la modification de la protection de page. Cet indicateur n’est valide que lorsque la protection passe à un type exécutable comme **page \_ Execute**, **page \_ Execute \_ Read**, **page \_ Execute \_ ReadWrite** et **page \_ Execute \_ WRITECOPY**. Le comportement par défaut pour la protection de **VirtualProtect** change en exécutable est de marquer tous les emplacements comme cibles d’appel valides pour cfg. <br/>                                           |



Les modificateurs suivants peuvent être utilisés en plus des options fournies dans le tableau précédent, sauf indication contraire.



| Constante/valeur                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**Page \_ PROTECTION**</dt> <dt>0x100</dt> </dl>                      | Les pages de la région sont des pages de garde. Toute tentative d’accès à une page de garde amène le système à déclencher une exception de **\_ violation de \_ page \_ Status Guard** et à désactiver l’état de la page de garde. Les pages de garde jouent donc un rôle d’alarme d’accès unique. Pour plus d’informations, consultez [Création de pages de garde](creating-guard-pages.md).<br/> Lorsqu’une tentative d’accès amène le système à désactiver l’état de la page de protection, la protection de la page sous-jacente prend le relais.<br/> Si une exception de page de garde se produit pendant un service système, le service retourne généralement un indicateur d’état d’échec.<br/> Cette valeur ne peut pas être utilisée avec **\_ l’accès** à la page.<br/> Cet indicateur n’est pas pris en charge par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**Page \_ NoCache**</dt> <dt>0x200</dt> </dl>                | Définit toutes les pages comme étant non cachable. Les applications ne doivent pas utiliser cet attribut, sauf s’ils sont explicitement requis pour un appareil. L’utilisation des fonctions verrouillées avec la mémoire mappée avec la valeur **s \_ NoCache** peut provoquer une exception d' **\_ \_ instruction illégale** .<br/> Impossible d’utiliser l’indicateur **page \_ NoCache** avec les indicateurs **page \_ Guard**, **page \_ NoAccess** ou **page \_ WRITECOMBINE** .<br/> L' **indicateur \_ NoCache de page** peut être utilisé uniquement lors de l’allocation de mémoire privée avec les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Pour activer l’accès à la mémoire non mis en cache pour la mémoire partagée, spécifiez l’indicateur **sec \_ NoCache** lors de l’appel de la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**Page \_ WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Définit toutes les pages à associer en écriture. <br/> Les applications ne doivent pas utiliser cet attribut, sauf s’ils sont explicitement requis pour un appareil. L’utilisation des fonctions bloquées avec la mémoire mappée en tant que combinaison d’écriture peut provoquer une exception d' **\_ \_ instruction non conforme** . <br/> L' **indicateur \_ WRITECOMBINE** de la page ne peut pas être spécifié avec les indicateurs **page \_ NoAccess**, **page \_ Guard** et **page \_ NoCache** . <br/> L' **indicateur \_ WRITECOMBINE de page** peut être utilisé uniquement lors de l’allocation de mémoire privée avec les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)ou [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Pour activer l’accès mémoire combiné en écriture pour la mémoire partagée, spécifiez l’indicateur **sec \_ WRITECOMBINE** lors de l’appel de la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/> **Windows Server 2003 et Windows XP :** cet indicateur n’est pas pris en charge jusqu’à Windows Server 2003 avec SP1.<br/> |



Les constantes suivantes peuvent uniquement être utilisées avec la fonction [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) lorsque vous spécifiez une enclave avec l’architecture Intel Software Guard extensions (SGX).



| Constante                                                                                                                                                                                                  | Description                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**contrôle de thread de l’enclave de PAGE \_ \_ \_**</dt> </dl> | La page contient une structure de contrôle de thread (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**ENCLAVE de PAGE non \_ \_ validée**</dt> </dl>           | Le contenu de la page que vous fournissez est exclu de la mesure avec l’instruction EEXTEND du modèle de programmation Intel SGX.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Protection de la mémoire](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
