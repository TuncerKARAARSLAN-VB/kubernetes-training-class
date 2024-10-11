# Kubectl pods command list

| **Komut**                                        | **Açıklama**                                         |
|--------------------------------------------------|-----------------------------------------------------|
| `kubectl get pods`                              | Tüm pod'ların listesini gösterir.                   |
| `kubectl get pods -n <namespace>`               | Belirtilen ad alanındaki tüm pod'ların listesini gösterir. |
| `kubectl describe pod <pod-adı>`                | Belirtilen pod hakkında ayrıntılı bilgi verir.      |
| `kubectl logs <pod-adı>`                         | Belirtilen pod'un günlüklerini gösterir.            |
| `kubectl logs <pod-adı> -c <container-adı>`     | Belirtilen pod'daki belirli bir konteynerin günlüklerini gösterir. |
| `kubectl exec -it <pod-adı> -- <komut>`         | Belirtilen pod içinde bir komut çalıştırır.         |
| `kubectl port-forward <pod-adı> <yerel-port>:<pod-port>` | Pod'a yerel bağlantı yönlendirir.                    |
| `kubectl delete pod <pod-adı>`                  | Belirtilen pod'u siler.                             |
| `kubectl scale --replicas=<sayı> pod/<pod-adı>` | Pod'un replikalarını ölçeklendirir.                 |
| `kubectl edit pod <pod-adı>`                    | Belirtilen pod'u düzenle.                           |
| `kubectl cp <pod-adı>:<dosya> <yerel-dosya>`    | Pod'dan yerel makineye dosya kopyalar.             |
| `kubectl get pods --field-selector=status.phase=Running` | Sadece çalışan pod'ların listesini alır.         |
| `kubectl get pods -o wide`                      | Pod'lar hakkında daha fazla bilgi ile birlikte gösterir (IP adresi, node bilgisi vb.). |
| `kubectl get pods --selector=<label-selector>`  | Belirtilen etiket seçicisi ile eşleşen pod'ların listesini gösterir. |
| `kubectl rollout restart pod/<pod-adı>`         | Pod'u yeniden başlatır.                             |
| `kubectl top pods`                               | Pod'ların kaynak kullanımını gösterir.              |

### Notlar:
- **Namespace Kullanımı:** Ad alanını belirtmek için `-n <namespace>` parametresini ekleyebilirsiniz.
- **Container Adı:** Eğer bir pod içinde birden fazla konteyner varsa, `-c <container-adı>` parametresini kullanarak belirli bir konteyner için işlem yapabilirsiniz.
- **Label Seçicileri:** `--selector=<label-selector>` ile etiket tabanlı sorgular yaparak spesifik pod'ları listeleyebilirsiniz.

Bu liste, `kubectl` ile pod'larla ilgili temel işlemleri hızlıca gerçekleştirmenize yardımcı olacaktır.