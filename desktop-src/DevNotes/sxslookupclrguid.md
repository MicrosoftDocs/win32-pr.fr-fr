---
description: Récupère le nom de la classe et d’autres informations associées à un GUID donné dans le manifeste d’un composant.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 6a23a9b761cca176e91650fab7c301a05c8e7435b2d46c97b1cdf1c1c5bc2027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103629"
---
# <a name="sxslookupclrguid-function"></a>SxsLookupClrGuid fonction)

Récupère le nom de la classe et d’autres informations associées à un GUID donné dans le manifeste d’un composant. Cette fonction est utilisée uniquement lors de l’implémentation de l’interopérabilité managée et non managée de bas niveau dans le .NET Framework. pour plus d’informations sur l’interopérabilité managée non managée, consultez « interopérabilité avec du Code non managé » dans le kit de développement logiciel (SDK) .NET Framework et également [Applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

## <a name="syntax"></a>Syntaxe


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Combinaison de zéro ou plusieurs des indicateurs suivants.



| Valeur                                                                                                                                                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ Rechercher \_ \_ GUID CLR \_ utiliser \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Si cet indicateur est défini, le paramètre *hActCtx* doit contenir un handle de contexte d’activation retourné par la fonction [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Si cet indicateur n’est pas défini, le paramètre *hActCtx* est ignoré et **SxsLookupClrGuid** recherche le contexte d’activation qui est actuellement actif (la fonction [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) est utilisée pour rendre un contexte d’activation actif).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ \_Rechercher un GUID CLR de recherche 0x00010000 de \_ \_ \_ substitution**</dt> <dt></dt> </dl>  | Si cet indicateur est défini, **SxsLookupClrGuid** recherche un substitut.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ RECHERCHE \_ \_ GUID CLR \_ Rechercher \_ la \_ classe CLR**</dt> <dt>0x00020000</dt> </dl> | Si cet indicateur est défini, **SxsLookupClrGuid** recherche une classe.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ RECHERCHE \_ du \_ GUID CLR \_ Rechercher \_ les**</dt> <dt>0x00030000</dt> </dl>                    | Il s’agit d’une combinaison de la recherche  **SxS \_ \_ \_ GUID CLR \_ \_** de recherche de substitut et de **\_ recherche SxS \_ GUID CLR Rechercher les indicateurs de \_ \_ \_ \_ classe CLR** ; si les deux sont définis, SxsLookupClrGuid recherche d’abord un substitut, et seulement s’il n’en trouve pas, puis recherche une classe.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ dans\]
</dt> <dd>

Pointeur vers le GUID sur lequel rechercher les informations d’interopérabilité dans le contexte d’activation. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*hActCtx* \[ dans, facultatif\]
</dt> <dd>

Si le **\_ GUID du CLR de recherche SxS \_ \_ \_ utilise \_** l’indicateur ACTCTX est défini dans le paramètre *dwFlags* , *hActCtx* doit contenir un handle de contexte d’activation retourné par la fonction [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Sinon, *hActCtx* est ignoré.

</dd> <dt>

*pvOutputBuffer* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers la mémoire tampon dans laquelle les informations de retour sont copiées. Ce paramètre peut avoir une valeur NULL uniquement si le paramètre *cbOutputBuffer* a une valeur zéro. Les données placées dans ce tampon à la sortie (le cas échéant) se composent d’une structure **\_ clr d' \_ informations \_ de GUID côte à côte** , suivie de toutes les données de chaîne supplémentaires requises. Pour plus d’informations, consultez la section Notes ci-dessous.

</dd> <dt>

*cbOutputBuffer* \[ dans\]
</dt> <dd>

Taille en octets de la mémoire tampon vers laquelle pointe le paramètre *pvOutputBuffer* .

</dd> <dt>

*pcbOutputBuffer* \[ à\]
</dt> <dd>

Pointeur vers une variable où la taille, en octets, des informations de retour est placée à la sortie. Si le paramètre *cbOutputBuffer* est égal à zéro, ou si la taille de la mémoire tampon de sortie est inférieure à la taille des informations de retour, **SxsLookupClrGuid** échoue et [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur de **\_ \_ mémoire tampon insuffisante**. Dans ce cas, utilisez la valeur de la variable vers laquelle pointe *pcbOutputBuffer* pour allouer une mémoire tampon suffisamment grande, puis appelez à nouveau **SxsLookupClrGuid** pour récupérer les informations souhaitées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire. Pour plus d’informations sur l’erreur, appelez [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Les composants managés peuvent se déclarer comme prenant en charge les « assemblys PIA » managés, afin de permettre à un consommateur de composant Win32 non managé de référencer l’assembly déclarant. Le consommateur du composant peut interagir avec le composant géré en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur un GUID. la couche d’interopérabilité achemine la demande de création d’objet à .NET Framework, crée une instance de l’objet managé et retourne un pointeur d’interface.

**SxsLookupClrGuid** permet aux frameworks de récupérer les informations associées à un GUID donné dans le manifeste du composant, telles que son nom de classe .net, la version du .NET Framework requis et l’assembly hôte dans lequel il se trouve. Les composants managés publient un assembly d’interopérabilité qui contient un certain nombre d’instructions associant des GUID à des noms d’assembly et de type, et le Runtime .NET fournit la construction d’instances d’objets managées quand [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) est appelé.

Voici un exemple de manifeste de composant déclarant un GUID CLR et un substitut CLR que **SxsLookupClrGuid** peut rechercher :

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Un fournisseur d’interopérabilité appelle **SxsLookupClrGuid** avec un pointeur vers le GUID « {fdb46ca5-9477-4528-b4b2-7f00a254cdea} » et reçoit dans le nom de classe « MySampleSurrogate », la version de Runtime requise « 1.0.3055 » et l’identité textuelle « dotnet. Sample. substituts, version = «1.0.0.0 », type = « Interop »» du composant d’hébergement.

Ces informations de retour sont contenues et/ou référencées par une structure **\_ clr d' \_ informations \_ de GUID SxS** déclarée comme suit.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

Les membres de cette structure contiennent les informations suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br/></td>
<td>Contient la taille de la structure de SXS_GUID_INFORMATION_CLR (cela permet à la structure de croître dans les versions ultérieures).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
<td>Contient l’une des deux valeurs d’indicateur suivantes : <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001) : indique que le GUID spécifié a été associé à un &quot; substitut.&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002) : indique que le GUID spécifié a été associé à une &quot; classe.&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br/></td>
<td>Pointe vers une chaîne de caractères larges se terminant par zéro qui identifie la version du runtime spécifiée dans le manifeste hôte pour cette classe.<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br/></td>
<td>Pointe vers une chaîne de caractères larges se terminant par zéro qui contient le nom de la classe .NET associée au GUID spécifié.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>Pointe vers une chaîne de caractères larges se terminant par zéro qui contient l’identité textuelle de l’assembly qui héberge cette classe. pour plus d’informations sur l’identité textuelle, consultez &quot; spécification de noms de types qualifiés complets &quot; sous &quot; découverte des informations de type au moment de &quot; l’exécution sous &quot; programmation avec l' .NET Framework &quot; dans le kit de développement logiciel (SDK) .NET Framework.<br/></td>
</tr>
</tbody>
</table>



 

une application non managée peut utiliser les informations retournées de cette façon pour charger la version appropriée du .NET Framework, charger l’assembly identifié par l’élément **pcwszAssemblyIdentity** , puis créer une instance de la classe nommée par l’élément **pcwszTypeName** .

## <a name="examples"></a>Exemples

Utilisez la liaison dynamique comme suit pour appeler la fonction **SxsLookupClrGuid** :


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll ; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
